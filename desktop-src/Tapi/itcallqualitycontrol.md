---
description: A interface ITCallQualityControl expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para controle de qualidade de chamada.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interface ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754190"
---
# <a name="itcallqualitycontrol-interface"></a>Interface ITCallQualityControl

\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITCallQualityControl** expõe métodos que permitem que um aplicativo obtenha e defina parâmetros para controle de qualidade de chamada.

Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e o [H323 MSP](h323-msp.md). Ele é exposto somente quando uma chamada usa esses provedores de serviços.

## <a name="members"></a>Membros

A interface **ITCallQualityControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITCallQualityControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITCallQualityControl** tem esses métodos.



| Método                                            | Descrição                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Obter**](itcallqualitycontrol-get.md)           | Obtém o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Obtém o intervalo de valores válidos para uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).<br/> |
| [**Definir**](itcallqualitycontrol-set.md)           | Define o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

