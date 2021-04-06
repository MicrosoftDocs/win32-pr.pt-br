---
description: A TAPI 3 envolve vários objetos que são independentes de seus cinco objetos principais da TAPI (TAPI, endereço, chamada, CallHub e terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objetos Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828331"
---
# <a name="stand-alone-objects"></a>Objetos Stand-Alone

A TAPI 3 envolve vários objetos que são independentes de seus cinco objetos principais da TAPI (TAPI, endereço, chamada, CallHub e terminal). [Interfaces de evento](./event-interfaces.md) e [interfaces de enumerador](enumerator-interfaces.md) são objetos autônomos e são resumidas separadamente. Veja a seguir um resumo das interfaces autônomas que não são de evento e não do enumerador.



| Interface                                             | Descrição                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | Fornece métodos para permitir que aplicativos cliente de automação, como Visual Basic, recuperem informações de coleção.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Estende o [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) fornecendo métodos adicionais para modificar coleções.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Interface COM padrão para implementar a automação.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Interface COM padrão para obter ponteiros para interfaces de objeto.                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Permite que um aplicativo recupere o ponteiro de expedição de outra interface em um objeto, dado um ponteiro atual do [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) . Útil para algumas linguagens de script. |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Fornece métodos que permitem que um aplicativo TAPI 3 Use [telefonia assistida](assisted-telephony-overview.md).                                                                                                |



 



| Interface                                  | Descrição                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Inicia, interrompe e pausa as ações atuais, como uma reprodução.                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Fornece métodos específicos de reprodução que permitem que um aplicativo execute essas operações como definir a lista de arquivos para reproduzir e alterar a velocidade de reprodução.              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Fornece métodos específicos de gravação que permitem que um aplicativo execute essas operações como definir os nomes dos arquivos para registrar e alterar a duração de uma gravação. |



 



| Interface                                                  | Descrição                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Recupera o formato de áudio do ou define o formato de áudio para um controle.                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Fornece métodos em objetos de terminal de áudio estáticos que são necessários para dar suporte a dispositivos de telefone. A TAPI 3,1 MSPs deve expor essa interface em todos os terminais de áudio estáticos. |



 

 

 
