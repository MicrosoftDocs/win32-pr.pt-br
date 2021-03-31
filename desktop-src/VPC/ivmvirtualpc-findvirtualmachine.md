---
title: Método IVMVirtualPC FindVirtualMachine (VPCCOMInterfaces. h)
description: Recupera um objeto de máquina virtual que corresponde à configuração solicitada.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- FindVirtualMachine do método virtual PC
- Método FindVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método FindVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086063"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a>Método IVMVirtualPC:: FindVirtualMachine

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um objeto de máquina virtual que corresponde à configuração solicitada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConfigurationName* \[ no\]
</dt> <dd>

O nome da máquina virtual a ser encontrada.

</dd> <dt>

*VirtualMachine* \[ out, retval\]
</dt> <dd>

Um ponteiro para um novo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1</dt> </dl>                                           | Não foi possível encontrar a configuração especificada.<br/>                                      |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *ConfigurationName* é inválido ou *VirtualMachine* é **nulo**.<br/>       |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.

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

 

