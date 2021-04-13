---
title: Propriedade UndoAction IVMVirtualMachine (VPCCOMInterfaces. h)
description: Ação padrão a ser executada em todas as unidades de desfazer quando a VM for desligada.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Propriedade UndoAction Virtual PC
- Propriedade UndoAction Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade UndoAction
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039a9e65863e41ba2c7edc1befd2598aa16bb362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455681"
---
# <a name="ivmvirtualmachineundoaction-property"></a>Propriedade IVMVirtualMachine:: UndoAction

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define a ação padrão a ser executada em todas as unidades de desfazer quando a VM (máquina virtual) for desligada usando [**o método de**](ivmvirtualmachine-turnoff.md) desativação ou desligar usando o método [**Shutdown**](ivmguestos-shutdown.md) ou desativado de dentro do sistema operacional convidado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica a ação padrão a ser executada em todas as unidades de desfazer quando a VM for desligada de dentro do sistema operacional convidado. Para obter uma lista de valores, consulte [**VMUndoAction**](vmundoaction.md).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | O parâmetro não é válido.<br/>       |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>     |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

