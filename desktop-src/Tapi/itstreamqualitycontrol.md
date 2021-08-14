---
description: O ITStreamQualityControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de qualidade de fluxo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interface ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4af57228cc7a91dad8232648d973d36a700b713d787f486e9f4a380bca6f6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863891"
---
# <a name="itstreamqualitycontrol-interface"></a>Interface ITStreamQualityControl

\[essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O **ITStreamQualityControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de qualidade de fluxo.

Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md). Ele é exposto somente quando uma chamada usa esses provedores de serviços.

## <a name="members"></a>Membros

A interface **ITStreamQualityControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITStreamQualityControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITStreamQualityControl** tem esses métodos.



| Método                                              | Descrição                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Obter**](itstreamqualitycontrol-get.md)           | Obtém o valor de uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Obtém o intervalo de valores válidos para uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).<br/> |
| [**Definição**](itstreamqualitycontrol-set.md)           | Define o valor de uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

