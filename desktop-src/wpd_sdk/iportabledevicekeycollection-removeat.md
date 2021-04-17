---
description: O método RemoveAt remove o elemento armazenado no local especificado pelo índice fornecido.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Método IPortableDeviceKeyCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797917"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a>Método IPortableDeviceKeyCollection:: RemoveAt

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

## <a name="return-value"></a>Retornar valor

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> </dl>

 

 




