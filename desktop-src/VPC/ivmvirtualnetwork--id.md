---
title: Método de _ID IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera o identificador interno da rede virtual.
ms.assetid: 6f1f75be-4218-40b8-8c73-938f0801f5e5
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMVirtualNetwork._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b79c4d6f4dfa778fee156b1bfa09ab39b8bedf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009667"
---
# <a name="ivmvirtualnetwork_id-method"></a>Método IVMVirtualNetwork:: \_ ID

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o identificador interno da rede virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT _ID(
  [out] VARIANT *virtualNetworkID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualNetworkID* \[ fora\]
</dt> <dd>

O identificador da rede virtual. O identificador para a rede virtual de rede compartilhada (NAT) é 01010101010101010101010101010101.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



 

## <a name="remarks"></a>Comentários

Essa propriedade não pode ser usada por linguagens de script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualNetwork**](ivmvirtualnetwork.md)
</dt> </dl>

 

