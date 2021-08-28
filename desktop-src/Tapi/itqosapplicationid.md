---
description: A interface ITQOSApplicationID expõe um método que permite que um aplicativo obtenha o identificador de QOS para a chamada atual.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interface ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126276"
---
# <a name="itqosapplicationid-interface"></a>Interface ITQOSApplicationID

\[essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITQOSApplicationID** expõe um método que permite que um aplicativo obtenha o identificador de QoS para a chamada atual.

Essa interface é implementada pelo [IPConf MSP](ipconf-msp.md) e é exposta somente quando uma chamada usa a conferência por IP.

## <a name="members"></a>Membros

A interface **ITQOSApplicationID** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITQOSApplicationID** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITQOSApplicationID** tem esses métodos.



| Método                                                                | Descrição                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Define o identificador de QOS.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

