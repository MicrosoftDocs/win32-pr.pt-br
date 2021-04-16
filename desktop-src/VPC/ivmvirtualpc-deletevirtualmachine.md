---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Exclui uma configuração de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine do método virtual PC
- Método DeleteVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794594"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC: método eleteVirtualMachine de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Exclui uma configuração de máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualMachine* \[ no\]
</dt> <dd>

Um ponteiro para um objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa a configuração da máquina virtual a ser excluída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1</dt> </dl>                                           | Não foi possível encontrar a configuração especificada.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *VirtualMachine* era **nulo**.<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt> </dl>                        | A máquina virtual está em execução.<br/>                                                      |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

Somente as máquinas virtuais interrompidas podem ser excluídas. Observe que qualquer estado salvo existente ou dados da unidade de desfazer para essa configuração serão excluídos além do arquivo de configuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

