---
title: Propriedade IVMVirtualMachineble (VPCCOMInterfaces. h)
description: Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- PC virtual de propriedade de desfazer
- Propriedade undoable Virtual PC, interface IVMVirtualMachine
- Virtual PC da interface IVMVirtualMachine, Propriedade undoable
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499400"
---
# <a name="ivmvirtualmachineundoable-property"></a>Propriedade IVMVirtualMachine:: undoable

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM (máquina virtual).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica a **variante \_ true** se as unidades de desfazer estiverem habilitadas para discos rígidos conectados à VM e **Variant \_ false** caso contrário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>     |
| <dl> <dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt> </dl> | A VM está em execução ou salva.<br/>       |



## <a name="remarks"></a>Comentários

Se as unidades de desfazer estiverem desabilitadas, qualquer arquivo de unidade de desfazer existente será excluído.

Você não poderá definir essa propriedade se a VM estiver em execução ou salva.

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

 

