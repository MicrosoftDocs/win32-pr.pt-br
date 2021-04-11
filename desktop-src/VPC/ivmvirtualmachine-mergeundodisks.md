---
title: Método IVMVirtualMachine MergeUndoDisks (VPCCOMInterfaces. h)
description: Mescla os discos de desfazer virtuais.
ms.assetid: 6445b097-220e-48c4-9a7b-1139ca7b3338
keywords:
- MergeUndoDisks do método virtual PC
- Método MergeUndoDisks Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método MergeUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.MergeUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48863bf998ebc02bac93aa9e74d8cdbe07265477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295861"
---
# <a name="ivmvirtualmachinemergeundodisks-method"></a>Método IVMVirtualMachine:: MergeUndoDisks

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Mescla os discos de desfazer virtuais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MergeUndoDisks(
  [out, retval] IVMTask **undoMergeTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*undoMergeTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar a criação da imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                            |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>                                                                                                   |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelo parâmetro *convertedDiskImagePath* ou um dos discos pai não é válido.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                               | O usuário atual não tem acesso suficiente ao arquivo pai.<br/>                                                                 |
| <dl> <dt>**E \_ MANIPULAR**</dt> <dt>0x80070006</dt> </dl>                                     | Um dos discos pai está em uso.<br/>                                                                                           |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                            | A configuração é desconhecida.<br/>                                                                                                |
| <dl> <dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt> </dl>                            | A máquina virtual está em execução.<br/>                                                                                              |
| <dl> <dt>**VM \_ E \_ File \_ \_ somente leitura**</dt> <dt>0xA004067A</dt> </dl>                       | O pai de discos de desfazer virtuais está marcado como somente leitura.<br/>                                                                     |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                            |



 

## <a name="remarks"></a>Comentários

**MergeUndoDisks** não pode ser chamado enquanto a máquina virtual ainda estiver em execução. Use [**IVMVirtualMachine:: Save**](ivmvirtualmachine-save.md) para salvar o estado da máquina virtual antes de chamar **MergeUndoDisks** ou [**IVMVirtualMachine::**](ivmvirtualmachine-turnoff.md) inativação para desligar a máquina virtual sem salvar seu estado atual antecipadamente.

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

 

