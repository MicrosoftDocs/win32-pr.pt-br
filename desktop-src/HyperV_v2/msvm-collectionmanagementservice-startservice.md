---
description: Método StartService da classe Msvm_CollectionManagementService – interrompe o serviço.
ms.assetid: 0f9a015d-b895-496a-a4c6-2737c0742746
title: Método StartService da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8f2e3a721ab21bc28ed97505f80a2da68aaca7e71db0847f95c288d032520a1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252736"
---
# <a name="startservice-method-of-the-msvm_collectionmanagementservice-class"></a>Método StartService da classe Msvm \_ CollectionManagementService

Interrompe o serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará 0 se for bem-sucedido; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




