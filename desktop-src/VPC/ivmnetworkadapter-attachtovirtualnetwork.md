---
title: Método IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Anexa a interface de rede à rede virtual especificada.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork do método virtual PC
- Método AttachToVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, método AttachToVirtualNetwork
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
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455303"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>Método IVMNetworkAdapter:: AttachToVirtualNetwork

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa a interface de rede à rede virtual especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualNetwork* \[ no\]
</dt> <dd>

A rede virtual à qual esta NIC virtual será conectada. Consulte [**IVMVirtualNetwork**](ivmvirtualnetwork.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                          | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                                                                       | A operação foi bem-sucedida.<br/>                           |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                  | O parâmetro é **NULL**.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | O parâmetro não contém uma rede virtual válida.<br/> |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt> </dl> | Acesso negado à rede virtual solicitada.<br/>     |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                          | A máquina virtual é inválida ou não existe mais.<br/>     |
| <dl> <dt>**\_ID da \_ \_ rede virtual \_ E da VM inválida \_**</dt> </dl>                                                                        | O parâmetro não é uma rede virtual existente.<br/>       |
| <dl> <dt>**obter \_ E \_ exceção**</dt> </dl>                                                                                          | Ocorreu um erro inesperado.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

