---
description: Coloca o serviço no estado iniciado.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Método StartService da classe CIM_Service (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0e30adbece838cb913f215abedc4aa86a2762d00f046a54bf2717eaeecdb56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561806"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Método StartService da classe CIM_Service (gerenciamento do Hyper-V)

Coloca o serviço no estado iniciado.

> [!Note]
>
> A semântica desse método se sobrepõe ao **método RequestStateChange** herdado de [**CIM \_ EnabledLogicalElement.**](cim-enabledlogicalelement.md) Esse método é mantido porque foi amplamente implementado e sua semântica simples de "início" é conveniente de usar.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ CIM**](cim-service.md)
</dt> </dl>

 

 




