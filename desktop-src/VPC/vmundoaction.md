---
title: Enumeração VMUndoAction (VPCCOMInterfaces. h)
description: Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desativada.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction de enumeração Virtual PC
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
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499750"
---
# <a name="vmundoaction-enumeration"></a>Enumeração VMUndoAction

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Especifica o que acontece para desfazer unidades quando uma máquina virtual é desligada ou desativada.

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

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**\_descartar vmUndoAction**
</dt> <dd>

Descartar as unidades de desfazer; as unidades pai permanecem inalteradas.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ manter**
</dt> <dd>

Manter as unidades de desfazer; as unidades pai permanecem inalteradas, mas as alterações serão mantidas na próxima vez que a máquina virtual for iniciada.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction \_ confirmação**
</dt> <dd>

Confirme as alterações nas unidades pai.

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

[**IVMVirtualMachine:: UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

