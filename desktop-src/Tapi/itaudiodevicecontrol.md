---
description: A interface ITAudioDeviceControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interface ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810140"
---
# <a name="itaudiodevicecontrol-interface"></a>Interface ITAudioDeviceControl

\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITAudioDeviceControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.

Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md). Ele é exposto quando uma chamada usa esses provedores de serviços ou um provedor de serviços de terceiros que implementa essa interface. Para obter um ponteiro para a interface **ITAudioDeviceControl** , chame **QueryInterface** na interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) que controla o dispositivo de áudio correspondente ao fluxo. O tipo de mídia da interface **ITStream** deve ser de áudio para que a interface **ITAudioDeviceControl** seja exposta.

## <a name="members"></a>Membros

A interface **ITAudioDeviceControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioDeviceControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITAudioDeviceControl** tem esses métodos.



| Método                                              | Descrição                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Obter**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtém o valor de uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtém o intervalo de valores válidos para uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).<br/> |
| [**Definir**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Define o valor de uma determinada [propriedade de dispositivo de áudio](audiodeviceproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

