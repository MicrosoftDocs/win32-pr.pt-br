---
description: Objetos de endereço são entidades que podem fazer ou receber chamadas. As interfaces e métodos relacionados permitem que um aplicativo obter e definir informações sobre um endereço, como se o endereço tem suporte à ID do chamador.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfaces de objeto de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2254ba47e81ebd40f5ce95a1c870c363d09243c69cec0c4ec358cf3ee5604de7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949172"
---
# <a name="address-object-interfaces"></a>Interfaces de objeto de endereço

[Objetos de](address-object.md) endereço são entidades que podem fazer ou receber chamadas. As interfaces e métodos relacionados permitem que um aplicativo obter e definir informações sobre um endereço, como se o endereço tem suporte à ID do chamador.

As interfaces [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation,**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation) [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)e [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) não são diretamente expostas no Objeto de Endereço, mas estão totalmente relacionadas a ele e são listadas aqui para conveniência de referência.



| Interface                                                            | Descrição                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Atua como interface base para o objeto Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Deriva de [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); fornece métodos adicionais que suportam dispositivos de telefone.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Obtém informações sobre as funcionalidades de um endereço.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Fornece informações sobre eventos de endereço.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Executa a conversão de endereços.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Obtém informações de conversão de endereço.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Fornece métodos para recuperar informações de cartão de chamada.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Fornece métodos para configurar e implementar o encaminhamento de chamada.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Dá suporte a aplicativos herdado que exigem acesso direto a um dispositivo e sua configuração.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Estende [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) permitindo a configuração de parâmetros relacionados a dispositivos de linha. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Obtém informações relacionadas ao local da parte de chamada.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Obtém informações sobre os recursos de suporte de mídia de um endereço.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Obtém informações sobre terminais disponíveis e fornece um método para criar terminais adicionais.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumera [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumera [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Se o endereço for um [endereço MSP](wave-msp.md) wave, a interface [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) também será exposta no objeto Address.

 

 
