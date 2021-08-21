---
description: Desabilita uma GPU física para virtualização.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Método DisableGPUForVirtualization da classe Msvm_Synthetic3DService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f156ee160f9ae158c36b1c7a237f746d6577906cc5e254a183308d5bec122a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150032"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>Método DisableGPUForVirtualization da classe Msvm \_ Synthetic3DService

Desabilita uma GPU física para virtualização.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PhysicalGPU* \[ Em\]
</dt> <dd>

Uma referência a uma instância da [**classe Msvm \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) que representa a GPU física a ser desabilitada.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ Synthetic3DService**](msvm-synthetic3dservice.md)
</dt> </dl>

 

