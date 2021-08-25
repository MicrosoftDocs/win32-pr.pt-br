---
description: O método ChangeType converte todos os itens na coleção para o VARTYPE especificado.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: Método IPortableDevicePropVariantCollection::ChangeType (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839326"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>Método IPortableDevicePropVariantCollection::ChangeType

O **método ChangeType** converte todos os itens na coleção para o VARTYPE especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vt* \[ Em\]
</dt> <dd>

Especifica o **VARTYPE** no qual você deseja converter todos os itens na coleção. Os tipos de exemplo incluem VT \_ UI4 e VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se esse método falhar, a coleção poderá ser deixada em um estado intermediário, com alguns membros convertidos e outros não convertidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




