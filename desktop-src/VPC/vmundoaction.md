---
title: Enumeração VMUndoAction (VPCCOMInterfaces.h)
description: Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desligada.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Computador Virtual de enumeração VMUndoAction
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f62c4ab00b30300b2951a5a6b1c300bf34b1b3797f036f28a66e82dc2cad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998326"
---
# <a name="vmundoaction-enumeration"></a>Enumeração VMUndoAction

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desligada.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction \_ Discard**
</dt> <dd>

Descartar as unidades de desfazer; as unidades pai permanecem inalteradas.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ Keep**
</dt> <dd>

Mantenha as unidades de desfazer; as unidades pai permanecem inalteradas, mas as alterações serão mantidas na próxima vez que a máquina virtual iniciar.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**VmUndoAction \_ Commit**
</dt> <dd>

Fazer commit das alterações nas unidades pai.

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

[**IVMVirtualMachine::UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

