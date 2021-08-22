---
description: Método IPortableDevicePropVariantCollection::RemoveAt – o método RemoveAt remove o elemento armazenado no local especificado pelo índice especificado.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: Método IPortableDevicePropVariantCollection::RemoveAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 311b3511329ed15f5afd83d5a84c0c5abd62fe3f44000962fbdcd2f8ddd67c9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026894"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>Método IPortableDevicePropVariantCollection::RemoveAt

O **método RemoveAt** remove o elemento armazenado no local especificado pelo índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

Especifica o índice do elemento a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice especificado estava fora do intervalo.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve especificar um índice baseado em zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




