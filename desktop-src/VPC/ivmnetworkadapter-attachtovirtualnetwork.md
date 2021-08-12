---
title: Método AttachToVirtualNetwork de IVMNetworkAdapter (VPCCOMInterfaces.h)
description: Anexa o interface de rede à rede virtual especificada.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork method Virtual PC
- AttachToVirtualNetwork method Virtual PC , IVMNetworkAdapter interface
- INTERFACE IVMNetworkAdapter Pc Virtual , método AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b03bf8bd0bcde6ba0353ce62e227c100a17ed1df0b2267ad54cd127c95c5836b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593224"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>Método IVMNetworkAdapter::AttachToVirtualNetwork

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa o interface de rede à rede virtual especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualNetwork* \[ Em\]
</dt> <dd>

A rede virtual à qual essa NIC virtual será conectada. Consulte [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                          | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | A operação foi bem-sucedida.<br/>                           |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                  | O parâmetro é **NULL.**<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | O parâmetro não contém uma rede virtual válida.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ACCESSNIED)**</dt> <dt>0X80070005</dt> </dl> | O acesso foi negado à rede virtual solicitada.<br/>     |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | A máquina virtual é inválida ou não existe mais.<br/>     |
| <dl> <dt>**VM \_ E \_ \_ \_ ID DE REDE VIRTUAL \_ INVÁLIDA**</dt> </dl>                                                                        | O parâmetro não é uma rede virtual existente.<br/>       |
| <dl> <dt>**EXCEÇÃO \_ DISP E \_**</dt> </dl>                                                                                          | Ocorreu um erro inesperado.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter é definido como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

