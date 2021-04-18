---
description: O ITStreamQualityControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para o controle de qualidade de fluxo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interface ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789857"
---
# <a name="itstreamqualitycontrol-interface"></a>Interface ITStreamQualityControl

\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

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
| [**Definir**](itstreamqualitycontrol-set.md)           | Define o valor de uma determinada [propriedade de qualidade de fluxo](streamqualityproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

