---
title: Enumeração vmFloppyDriveEvent (VPCCOMInterfaces.h)
description: Especifica os eventos de unidade de disquete.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- VmFloppyDriveEvent enumeration Virtual PC
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f8ded5cf87d740f113bab54d9f7587c8f8927e5ae37352dceb4a30be09d104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767896"
---
# <a name="vmfloppydriveevent-enumeration"></a>Enumeração vmFloppyDriveEvent

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica os eventos de unidade de disquete.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent \_ OnInsert**
</dt> <dd>

Uma imagem de disquete é anexada ou a mídia real é inserida em uma unidade de host.

</dd> <dt>

<span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ OnEject**
</dt> <dd>

A mídia foi ejetada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

