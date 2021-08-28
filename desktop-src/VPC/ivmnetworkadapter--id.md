---
title: Método de _ID IVMNetworkAdapter (VPCCOMInterfaces.h)
description: Recupera o identificador interno desse interface de rede.
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID computador virtual do método
- _ID método Virtual PC, interface IVMNetworkAdapter
- Interface IVMNetworkAdapter pc virtual , _ID método
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42e374418fce3a0d6352514c48e883c5ce51e811a83bd3c030a1c5361119bf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753065"
---
# <a name="ivmnetworkadapter_id-method"></a>MÉTODO IVMNetworkAdapter:: \_ ID

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o identificador interno desse interface de rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*identificador* \[ out\]
</dt> <dd>

O identificador interno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                 | Descrição                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>           |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | A máquina virtual não pode ser encontrada.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | A operação teve um erro desconhecido.<br/>  |



 

## <a name="remarks"></a>Comentários

Esse método não pode ser usado por linguagens de script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMNetworkAdapter é definido como \_ e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

