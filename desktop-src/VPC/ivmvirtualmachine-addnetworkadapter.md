---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Adiciona uma interface de rede à máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter do método virtual PC
- Método AddNetworkAdapter Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763806"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>Método IVMVirtualMachine:: AddNetworkAdapter

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Adiciona uma interface de rede à máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*adaptador* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                            | Descrição                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | A operação foi bem-sucedida.<br/>                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                    | O parâmetro *adaptador* é **nulo**.<br/>          |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>            | A configuração é desconhecida.<br/>                        |
| <dl> <dt>**VM \_ E \_ pref \_ \_ valor ilegal**</dt> <dt>0xA0040301</dt> </dl>   | Não é possível adicionar mais de quatro (4) adaptadores de rede.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ em execução \_ ou \_ salvas**</dt> <dt>0xA004020B</dt> </dl> | A máquina virtual está em um estado em execução ou salvo.<br/>  |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>            | Ocorreu um erro inesperado.<br/>                    |



 

## <a name="remarks"></a>Comentários

Você só pode adicionar uma nova interface de rede a uma máquina virtual parada. O adaptador de rede recém-criado não está conectado a uma rede virtual.

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

 

