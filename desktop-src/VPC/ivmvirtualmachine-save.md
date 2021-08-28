---
title: Método IVMVirtualMachine Save (VPCCOMInterfaces.h)
description: Salva o estado da VM (máquina virtual).
ms.assetid: e9f6e773-4e2d-4d7b-9624-e7864d5b248b
keywords:
- Salvar o computador virtual do método
- Save method Virtual PC , IVMVirtualMachine interface
- INTERFACE IVMVirtualMachine pc virtual, método Save
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Save
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609125ed9ae8deab897163d6a841e9cb665659c2c5af76baff3a1d96fb235e92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124786"
---
# <a name="ivmvirtualmachinesave-method"></a>Método IVMVirtualMachine::Save

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Salva o estado da VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Save(
  [out, retval] IVMTask **saveTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*saveTask* \[ out, retval\]
</dt> <dd>

Um [**objeto IVMTask**](ivmtask.md) usado para acompanhar o progresso da conclusão da sequência de economia de estado da VM.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                          | Descrição                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | A operação foi bem-sucedida.<br/>                                                 |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0X80004005</dt> </dl>                                     | Não foi possível salvar a VM porque os discos de desfazer foram marcados para exclusão.<br/>    |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                  | O parâmetro é **NULL.**<br/>                                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ACCESSNIED)**</dt> <dt>0X80070005</dt> </dl> | O chamador deve ter permissões de acesso de execução para salvar o estado dessa VM.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>                     | A VM não está em execução.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ocorreu um erro inesperado.<br/>                                             |



 

## <a name="remarks"></a>Comentários

A VM é desligada quando a **tarefa Salvar** atinge a conclusão. A [**propriedade IVMVirtualMachine::State**](ivmvirtualmachine-state.md) conterá **vmVMState \_ Saving** enquanto o salvar estiver em andamento, seguido por **vmVMState \_ Salvo** quando o salvar for concluído e a VM estiver desligada.

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

 

