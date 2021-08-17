---
title: Propriedade Undoable IVMVirtualMachine (VPCCOMInterfaces.h)
description: Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Propriedade desfavelável Pc Virtual
- Propriedade desfazível Pc Virtual , interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , propriedade desfazível
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
ms.openlocfilehash: f7663cefb8f94809f0fd016e002102c9956066b64ca21fb79766598b592ec3dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752069"
---
# <a name="ivmvirtualmachineundoable-property"></a>Propriedade IVMVirtualMachine::Undoable

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se as unidades de desfazer estão habilitadas para discos rígidos conectados à VM (máquina virtual).

Essa propriedade é leitura/gravação.

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

Especifica **VARIANT \_ TRUE se** as unidades de desfazer estão habilitadas para discos rígidos conectados à VM e VARIANT **\_ FALSE** caso contrário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ocorreu um erro inesperado.<br/> |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>              | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | A configuração é desconhecida.<br/>     |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | A VM está em execução ou salva.<br/>       |



## <a name="remarks"></a>Comentários

Se as unidades de desfazer estão desabilitadas, todos os arquivos de unidade de desfazer existentes serão excluídos.

Você não poderá definir essa propriedade se a VM estiver em execução ou salva.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

