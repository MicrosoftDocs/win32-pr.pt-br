---
description: O método SetIPortableDeviceKeyCollectionValue adiciona um novo valor SetIPortableDeviceKeyCollectionValue (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Método IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786251"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a>Método IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue

O método **SetIPortableDeviceKeyCollectionValue** adiciona um novo valor **SETIPORTABLEDEVICEKEYCOLLECTIONVALUE** (tipo VT \_ desconhecido) ou substitui um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.

</dd> <dt>

*valores* \[ no\]
</dt> <dd>

Ponteiro para uma interface **IPortableDeviceKeyCollection** que especifica o novo valor. O SDK copia uma referência para a interface enviada e chama **AddRef** nela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




