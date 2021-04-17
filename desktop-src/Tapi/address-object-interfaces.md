---
description: Os objetos de endereço são entidades que podem fazer ou receber chamadas. As interfaces e os métodos relacionados permitem que um aplicativo obtenha e defina informações relacionadas a um endereço, como se o endereço tem suporte para ID do chamador.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfaces de objeto de endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef19db02123e10e839906a00931ef246d19d2c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761364"
---
# <a name="address-object-interfaces"></a>Interfaces de objeto de endereço

Os [objetos de endereço](address-object.md) são entidades que podem fazer ou receber chamadas. As interfaces e os métodos relacionados permitem que um aplicativo obtenha e defina informações relacionadas a um endereço, como se o endereço tem suporte para ID do chamador.

As interfaces [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)e [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) não são diretamente expostas no objeto address, mas estão intimamente relacionadas a ela e estão listadas aqui para conveniência de referência.



| Interface                                                            | Descrição                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Atua como interface base para o objeto de endereço.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Deriva de [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); fornece métodos adicionais que dão suporte a dispositivos telefônicos.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Obtém informações sobre os recursos de um endereço.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Fornece informações relacionadas a eventos de endereço.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Executa a conversão de endereços.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Obtém informações de conversão de endereço.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Fornece métodos para recuperar informações de cartão de chamada.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Fornece métodos para configurar e implementar o encaminhamento de chamadas.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Dá suporte a aplicativos herdados que exigem acesso direto a um dispositivo e sua configuração.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Estende o [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) permitindo a configuração de parâmetros relacionados a dispositivos de linha. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Obtém informações relacionadas ao local da entidade de chamada.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Obtém informações sobre os recursos de suporte de mídia de um endereço.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Obtém informações sobre terminais disponíveis e fornece um método para criar terminais adicionais.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumera [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumera [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Se o endereço for um endereço [msp de onda](wave-msp.md) , a interface [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) também será exposta no objeto de endereço.

 

 
