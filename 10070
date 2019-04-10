// Versión
var  VERSION  =  ' $ {VERSION-0.2.0} ' ;

// Literales
var  MSG_RELLENAR_ENTRADA  =  ' Primero debes introducir los datos requeridos ' ;

// Valores
var  SITUACION_VISITA_CONCERTADA  =  ' Visita concertada ' ;

// Argumentos
var  ARG_FECHA_VISITA  =  ' Fecha visita ' ;

// Librerias
var  LIB_PERSONAL  =  ' Personal '
var  LIB_CENTROS  =  ' Centros 10070 ' ;
var  LIB_FICHA  =  ' Ficha 10070 ' ;
var  LIB_VISITA  =  ' Control visita 10070 ' ;
//var  LIB_PRESION  =  ' Presión arterial ' ;
var  LIB_COMPLEMENTO_ASIGNADO  =  ' Complementos asignados 10070 ' ;
var  LIB_DIETA_ASIGNADA  =  ' Dietas asignadas 10070' ;

// Campos generales - Todas las librerias los tienen
var  CAMPO_NUM_REG  =  ' numReg ' ;
var  CAMPO_COD_REG  =  ' codReg ' ;

// Campos por libreria

// Personal
var  LIB_PERSONAL_CAMPO_IDPERSONAL  =  ' idPersonal '

// Centros
var  LIB_CENTROS_CAMPO_FICHA_CLIENTE  =  ' Ficha cliente ' ;
var  LIB_CENTROS_CAMPO_IDDIETISTA  =  ' iddietista ' ;

// Ficha
var  LIB_FICHA_CAMPO_SITUACION  =  ' Situación ' ;
var  LIB_FICHA_CAMPO_MEDICIONES_PRESION_ARTERIAL  =  ' Mediciones Presión arterial ' ;
var  LIB_FICHA_CAMPO_VISITA  =  ' Visita ' ;
var  LIB_FICHA_CAMPO_IDCENTRO  =  ' idCentro ' ;
var  LIB_FICHA_CAMPO_IDDIETISTA  =  ' iddietista ' ;

// visita
var  LIB_VISITA_CAMPO_DFICHPACIENTE  =  ' dFichPaciente ' ;
var  LIB_VISITA_CAMPO_FECHA_VISITA  =  ' Fecha visita ' ;
var  LIB_VISITA_CAMPO_SITUACION  =  ' Situación ' ;
var  LIB_VISITA_CAMPO_CONTROL_VISITA  =  ' Control visita ' ;
var  LIB_VISITA_CAMPO_DDIETISTA  =  ' dDietista ' ;
var  LIB_VISITA_CAMPO_DCENTRO  =  ' dCentro ' ;
var  LIB_VISITA_CAMPO_DIETA_ANTERIOR  =  ' Dieta Anterior ' ;
var  LIB_VISITA_CAMPO_DIETA_ASIGNADA  =  ' Dieta Asignada ' ;
var  LIB_VISITA_CAMPO_COMPLEMENTO_ANTERIOR  =  ' Complemento Anterior ' ;
var  LIB_VISITA_CAMPO_COMPLEMENTOS_PRESCRITOS  =  ' Complementos Prescritos ' ;

// Presion
// var  LIB_PRESION_CAMPO_IDFICHA  =  ' idFicha ' ;
// var  LIB_PRESION_CAMPO_IDDIETISTA  =  ' idDietista ' ;

// Complemento asignado
var  LIB_COMPLEMENTO_ASIGNADO_CAMPO_VISITA  =  ' idVisita ' ;
var  LIB_COMPLEMENTO_ASIGNADO_CAMPO_IDDIETISTA  =  ' idDietista ' ;

// Dieta asignada
var  LIB_DIETA_ASIGNADA_CAMPO_VISITA  =  ' idVisita ' ;
var  LIB_DIETA_ASIGNADA_CAMPO_IDDIETISTA  =  ' idDietista ' ;



var cacheLinks = {};

función  setLink ( entrada , campo , entradaALinkar ) {
    var cacheLink =  getLink (entrada, campo);

    cacheLink . unshift (entradaALinkar);
    entrada . enlace (campo, entradaALinkar);

    cacheLinks [ entrada . id  +  '  '  + campo] = cacheLink;
}

funcion  removeLink ( entrada , campo , entradaADesLinkar ) {
    var cacheLink =  getLink (entrada, campo);

    cacheLink =  cacheLink . filtro ( función ( el ) {
        volver  el . id  ! ==  entradaADesLinkar . Identificación ;
    });
    entrada . desvincular (campo, entradaADesLinkar);

    cacheLinks [ entrada . id  +  '  '  + campo] = cacheLink;
}

función  getLink ( entrada , campo ) {
    if (cacheLinks [ entrada . id  +  '  '  + campo] ==  null ) {
        cacheLinks [ entrada . id  +  '  '  + campo] =  entrada . campo (campo);
    }

    devolver cacheLinks [ entrada . id  +  '  '  + campo];
}

función  getField ( entrada , campo ) {
    prueba {
        var valor =  entrada . campo (campo);
        // Si es un link cacheado
        if (cacheLinks [ entrada . id  +  '  '  + campo] ! =  null ) {
            volver  getLink (entrada, campo);
        }
        valor de retorno
    } atrapar (e) {
        mensaje (campo +  ' - '  + e);
        mensaje (campo +  ' - '  + e);
        mensaje (campo +  ' - '  +  e . stack );
        mensaje (campo +  ' - '  +  e . stack );
        lanzar e;
    }
}


función  getLibreria ( libreria ) {
    if (libreria ==  null ) {
        libreria =  lib ();
    } Demás  si ( typeof libreria ==  ' cadena ' ) {
        libreria =  libByName (libreria);
    }
    volver libreria;
}

función para  cada ( coleccion , funcion ) {
    if (coleccion ! =  null  &&  coleccion . length  ! =  0 ) {
        para ( var i =  0 ; i <  coleccion . length ; i ++ ) {
            funcion (coleccion [i], i);
        }
    }
}

Función  completarFicha ( centro , ficha , entradaMaestro ) {
    // crearVisita ({}, ficha, LIB_FICHA_CAMPO_VISITA, entradaMaestro);
}

Función  completarVisita ( ficha , visita , entradaMaestro ) {
    prueba {
        setLink (visita, LIB_VISITA_CAMPO_DCENTRO , getField (ficha, LIB_FICHA_CAMPO_IDCENTRO ) [ 0 ]);
    } atrapar (e) {
        mensaje (e);
        mensaje (e);
        mensaje (e);
        lanzar e;
    }
}

Función  completarPresion ( ficha , presion , entradaMaestro ) {
    // Nada que hacer
}

Función  completarComplementoAsignado ( visita , complementoAsignado , entradaMaestro ) {
    // Nada que hacer
}

Función  completarDietaAsignada ( visita , dietaAsignada , entradaMaestro ) {
    // Dieta anterior?
}

function  crearFicha ( objetoEntrada , entradaPadre , campoLinkPadre , entradaMaestro ) {
    return  crearEntrada ( LIB_FICHA , objetoEntrada, completarFicha, LIB_FICHA_CAMPO_IDCENTRO , entradaPadre, campoLinkPadre, entradaMaestro, LIB_FICHA_CAMPO_IDDIETISTA );
}

function  crearVisita ( objetoEntrada , entradaPadre , campoLinkPadre , entradaMaestro ) {
    return  crearEntrada ( LIB_VISITA , objetoEntrada, completarVisita, LIB_VISITA_CAMPO_DFICHPACIENTE , entradaPadre, campoLinkPadre, entradaMaestro, LIB_VISITA_CAMPO_DDIETISTA );
}

function  crearPresion ( objetoEntrada , entradaPadre , campoLinkPadre , entradaMaestro ) {
    return  crearEntrada ( LIB_PRESION , objetoEntrada, completarPresion, LIB_PRESION_CAMPO_IDFICHA , entradaPadre, campoLinkPadre, entradaMaestro, LIB_PRESION_CAMPO_IDDIETISTA );
}

función  crearComplementoAsignado ( objetoEntrada , entradaPadre , campoLinkPadre , entradaMaestro ) {
    return  crearEntrada ( LIB_COMPLEMENTO_ASIGNADO , objetoEntrada, completarPresion, LIB_COMPLEMENTO_ASIGNADO_CAMPO_VISITA , entradaPadre, campoLinkPadre, entradaMaestro, LIB_COMPLEMENTO_ASIGNADO_CAMPO_IDDIETISTA );
}

function  crearDietaAsignada ( objetoEntrada , entradaPadre , campoLinkPadre , entradaMaestro ) {
    return  crearEntrada ( LIB_DIETA_ASIGNADA , objetoEntrada, completarPresion, LIB_DIETA_ASIGNADA_CAMPO_VISITA , entradaPadre, campoLinkPadre, entradaMaestro, LIB_DIETA_ASIGNADA_CAMPO_IDDIETISTA );
}


/ **
 * 
* @param  {Library | String}  libreria Libreria donde se debe crear la entrada
* @param  {Objeto}  objetoEntrada Objeto a partir del cual se debe crear la nueva entrada
* @param  {Función}  funcionCompletarEntrada Funciona como se debe llamar para completar el objeto creado
* @param  {String}  campoLink Campo de la libreria donde creamos la entrada que debe enlazar con la entrada padre
* @param  {Entrada}  entradaPadre Entrada padre con la que debe estar el enlace bidireccionalmente
* @param  {String}  campoLinkPadre Campo de la entrada padre donde debe estar el enlace a la entrada nueva
* @param  {Entrada}  entradaMaestro Entrada maestro que con la que debemos vincular
* @param  {String}  campoMaestro Campo de la entrada maestro que debemos enlazar
 * /
function  crearEntrada ( libreria , objetoEntrada , funcionCompletarEntrada , campoLink , entradaPadre , campoLinkPadre , entradaMaestro , campoMaestro ) {
    libreria =  getLibreria (libreria);
    var entrada =  libreria . crear (objetoEntrada);

    entrada . conjunto ( CAMPO_NUM_REG , 0 );

    entrada . set ( CAMPO_COD_REG , construirCodReg (entrada, entradaPadre));

    setLink (entrada, campoMaestro, entradaMaestro);
    setLink (entrada, campoLink, entradaPadre);
    setLink (entradaPadre, campoLinkPadre, entrada);

    if (funcionCompletarEntrada ! =  null ) {
        funcionCompletarEntrada (entradaPadre, entrada, entradaMaestro);
    }

    entrada . recalc ();
    entradaPadre . recalc ();

    volver entrada
}

funcion  accionCentroCrearFicha ( centro ) {
    if (centro ==  null ) {
        centro =  entrada ();
    }

    var funcionCrearEntrada = crearFicha;
    var campoLink =  LIB_CENTROS_CAMPO_FICHA_CLIENTE ;
    var entradaMaestro =  getField (centro, LIB_CENTROS_CAMPO_IDDIETISTA ) [ 0 ];

    accionCrearEntrada (centro, funcionCrearEntrada, campoLink, entradaMaestro);
}

funcion  accionFichaCrearVisita ( ficha ) {

    si (ficha ==  nula ) {
        ficha =  entrada ();
    }

    var funcionCrearEntrada = crearVisita;
    var campoLink =  LIB_FICHA_CAMPO_VISITA ;
    var entradaMaestro =  getField (ficha, LIB_FICHA_CAMPO_IDDIETISTA ) [ 0 ];

    var visita =  accionCrearEntrada (ficha, funcionCrearEntrada, campoLink, entradaMaestro);

    if (visita ! =  null ) {
        var fechaVisita =  arg ( ARG_FECHA_VISITA );
        if (fechaVisita ==  null ) {
            fechaVisita =  new  Date ();
        }

        una visita . conjunto ( LIB_VISITA_CAMPO_FECHA_VISITA , fechaVisita);
        una visita . conjunto ( LIB_VISITA_CAMPO_SITUACION , SITUACION_VISITA_CONCERTADA );
        una visita . recalc ();
    }
}

función  accionFichaCrearPresion ( ficha ) {
    si (ficha ==  nula ) {
        ficha =  entrada ();
    }

    var funcionCrearEntrada = crearPresion;
    var campoLink =  LIB_FICHA_CAMPO_MEDICIONES_PRESION_ARTERIAL ;
    var entradaMaestro =  getField (ficha, LIB_FICHA_CAMPO_IDDIETISTA ) [ 0 ];

    accionCrearEntrada (ficha, funcionCrearEntrada, campoLink, entradaMaestro);
}

Función  accionVisitaCrearComplementoAsignado ( visita ) {
    if (visita ==  null ) {
        visita =  entrada ();
    }

    var funcionCrearEntrada = crearComplementoAsignado;
    var campoLink =  LIB_VISITA_CAMPO_COMPLEMENTOS_PRESCRITOS ;
    var entradaMaestro =  getField (visita, LIB_VISITA_CAMPO_DDIETISTA ) [ 0 ];

    accionCrearEntrada (visita, funcionCrearEntrada, campoLink, entradaMaestro);
}

funcion  accionVisitaCrearDietaAsignada ( visita ) {
    if (visita ==  null ) {
        visita =  entrada ();
    }

    var funcionCrearEntrada = crearDietaAsignada;
    var campoLink =  LIB_VISITA_CAMPO_DIETA_ASIGNADA ;
    var entradaMaestro =  getField (visita, LIB_VISITA_CAMPO_DDIETISTA ) [ 0 ];

    accionCrearEntrada (visita, funcionCrearEntrada, campoLink, entradaMaestro);
}

function  accionCrearEntrada ( entradaActual , funcionCrearEntrada , campoLink , entradaMaestro ) {
    if (entradaActual ==  null ) {
        entradaActual =  entry ();
    }

    var entradaNueva =  null ;

    if ( getField (entradaActual, CAMPO_NUM_REG ) ==  0 ) {
        msg ( MSG_RELLENAR_ENTRADA );
    } else {
        var entradaNueva =  null ;

        var entradasHijo =  getField (entradaActual, campoLink);

        forEach (entradasHijo, function ( entrada ) {
            if ( getField (entrada, CAMPO_NUM_REG ) ==  0 ) {
                entradaNueva = entrada;
            }
        });

        if (entradaNueva ==  null ) {
            entradaNueva =  funcionCrearEntrada ({}, entradaActual, campoLink, entradaMaestro);
        }

        entradaNueva . show ();
    }

    volver entradaNueva;
}

Función  disparadorDespuesModificarFicha () {
    disparadorModificarEntrada ( LIB_FICHA_CAMPO_IDCENTRO );
}

Función  disparadorDespuesModificarVisita () {
    disparadorModificarEntrada ( LIB_VISITA_CAMPO_DFICHPACIENTE );
}

función  disparadorDespuesModificarPresion () {
    disparadorModificarEntrada ( LIB_PRESION_CAMPO_IDFICHA );
}

Función  disparadorDespuesModificarComplementoAsignado () {
    disparadorModificarEntrada ( LIB_COMPLEMENTO_ASIGNADO_CAMPO_VISITA );
}

Función  disparadorDespuesModificarDietaAsignada () {
    disparadorModificarEntrada ( LIB_DIETA_ASIGNADA_CAMPO_VISITA );
}

Función  disparadorModificarEntrada ( campoPadre , libreria , entradaActual ) {
    if (entradaActual ==  null ) {
        entradaActual =  entry ();
    }
    libreria =  getLibreria (libreria);

    if ( getField (entradaActual, CAMPO_NUM_REG ) ==  0 ) {
        EntradaActual . set ( CAMPO_NUM_REG , obtenerSiguienteId (libreria));

        var entradaPadre =  getField (entradaActual, campoPadre) [ 0 ];
        EntradaActual . set ( CAMPO_COD_REG , construirCodReg (entradaActual, entradaPadre));
        
        EntradaActual . recalc ();
    }
}

function  construirCodReg ( entrada , entradaPadre ) {
    devuelve  getField (entradaPadre, CAMPO_COD_REG ) +  ' - '  +  getField (entrada, CAMPO_NUM_REG );
}

función  obtenerSiguienteId ( libreria ) {
    libreria =  getLibreria (libreria);

    var maxId =  0 ;

    var entradas =  libreria . entradas ();
    forEach (entradas, función ( entrada ) {
        var num =  getField (entrada, CAMPO_NUM_REG );
        if (num > maxId) {
            maxId = num;
        }
    });

    devuelve maxId +  1 ;
}

función  msg ( mensaje ) {
    mensaje (mensaje);
    mensaje (mensaje);
    mensaje (mensaje);
}

 versión de la función () {
    msg ( VERSION );
}


