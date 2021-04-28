---
description: 'Método IPortableDevicePropVariantCollection:: RemoveAt – o método RemoveAt remove o elemento armazenado no local especificado pelo índice fornecido.'
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Método IPortableDevicePropVariantCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109935"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>Método IPortableDevicePropVariantCollection:: RemoveAt

O método **RemoveAt** remove o elemento armazenado no local especificado pelo índice fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Especifica o índice do elemento a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice especificado estava fora do intervalo.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve especificar um índice com base em zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




