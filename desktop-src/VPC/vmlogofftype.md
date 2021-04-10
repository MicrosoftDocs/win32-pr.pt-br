---
title: Enumeração VMLogoffType (VPCCOMInterfaces. h)
description: Especifica como desligar uma máquina virtual.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- VMLogoffType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009324"
---
# <a name="vmlogofftype-enumeration"></a>Enumeração VMLogoffType

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica como desligar uma máquina virtual (VM).

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**
</dt> <dd>

O logoff na VM convidada foi normal.

</dd> <dt>

<span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forçado**
</dt> <dd>

O logoff na VM convidada foi forçado.

</dd> <dt>

<span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externo**
</dt> <dd>

O logoff na VM convidada foi feito usando o método [**IVMGuestOS:: logoff**](ivmguestos-logoff.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

