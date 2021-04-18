---
description: A interface ITAudioSettings expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interface ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784093"
---
# <a name="itaudiosettings-interface"></a>Interface ITAudioSettings

\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITAudioSettings** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de um dispositivo de áudio.

Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md). Ele é exposto somente quando uma chamada usa esses provedores de serviços.

## <a name="members"></a>Membros

A interface **ITAudioSettings** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioSettings** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITAudioSettings** tem esses métodos.



| Método                                              | Descrição                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Obter**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtém o valor de uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtém o intervalo de valores válidos para uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).<br/> |
| [**Definir**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Define o valor de uma determinada [propriedade de configuração de áudio](audiosettingsproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

