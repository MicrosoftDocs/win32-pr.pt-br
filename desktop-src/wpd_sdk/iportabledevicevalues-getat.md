---
description: O método GetAt recupera um valor da coleção usando o índice de base zero fornecido.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Método IPortableDeviceValues:: GetAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747651"
---
# <a name="iportabledevicevaluesgetat-method"></a>Método IPortableDeviceValues:: GetAt

O método **GetAt** recupera um valor da coleção usando o índice de base zero fornecido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

Um **DWORD** que especifica um índice de base zero na coleção.

</dd> <dt>

*pKey* \[ entrada, saída\]
</dt> <dd>

Um ponteiro de **PROPERTYKEY** opcional que recupera a chave do item especificado.

</dd> <dt>

*valores* \[ entrada, saída\]
</dt> <dd>

Um **PROPVARIANT** opcional que recupera o valor do item especificado. O chamador deve liberar a memória chamando **PropVariantClear** quando terminar com ela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um número de índice inválido foi especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Se uma propriedade indicar um valor do tipo VT \_ desconhecido, a propriedade será um dos dispositivos portáteis do Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) ou [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Nenhuma outra interface pode ser retornada por dispositivos portáteis do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




