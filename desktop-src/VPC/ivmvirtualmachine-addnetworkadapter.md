---
title: Método IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces.h)
description: Adiciona um interface de rede à máquina virtual.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Computador Virtual do método AddNetworkAdapter
- Método AddNetworkAdapter Pc Virtual , interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , método AddNetworkAdapter
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
ms.openlocfilehash: 799aa859ab8cd2bea4da29154af00c6537bfd180b0719f6d0252b1b0ddea8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866726"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a>Método IVMVirtualMachine::AddNetworkAdapter

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Adiciona um interface de rede à máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*networkAdapter* \[ out, retval\]
</dt> <dd>

Um [**objeto IVMNetworkAdapter.**](ivmnetworkadapter.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                            | Descrição                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | A operação foi bem-sucedida.<br/>                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                    | O *parâmetro networkAdapter* é **NULL.**<br/>          |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>            | A configuração é desconhecida.<br/>                        |
| <dl> <dt>**VM \_ E \_ PREF \_ ILLEGAL VALUE \_ 0XA0040301**</dt> <dt></dt> </dl>   | Não é possível adicionar mais de quatro (4) adaptadores de rede.<br/> |
| <dl> <dt>**VM \_ VM \_ E EM EXECUÇÃO OU SALVA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl> | A máquina virtual está em um estado de execução ou salvo.<br/>  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>            | Ocorreu um erro inesperado.<br/>                    |



 

## <a name="remarks"></a>Comentários

Você só pode adicionar um novo interface de rede a uma máquina virtual interrompida. O adaptador de rede recém-criado não está conectado a uma rede virtual.

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

 

