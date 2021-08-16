---
description: O método GetAt recupera um valor da coleção usando o índice baseado em zero fornecido.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: Método IPortableDeviceValues::GetAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843019"
---
# <a name="iportabledevicevaluesgetat-method"></a>Método IPortableDeviceValues::GetAt

O **método GetAt** recupera um valor da coleção usando o índice baseado em zero fornecido.

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

*índice* \[ Em\]
</dt> <dd>

Um **DWORD** que especifica um índice baseado em zero na coleção.

</dd> <dt>

*pKey* \[ in, out\]
</dt> <dd>

Um ponteiro **PROPERTYKEY** opcional que recupera a chave do item especificado.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Um **PROPVARIANT opcional** que recupera o valor do item especificado. O chamador deve liberar a memória chamando **PropVariantClear** quando terminar de fazer isso.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um número de índice inválido foi especificado.<br/> |



 

## <a name="remarks"></a>Comentários

Se uma propriedade indicar um valor do tipo VT UNKNOWN, a propriedade será um dos Dispositivos Portáteis \_ do Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) ou [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Nenhuma outra interface pode ser retornada por Windows Dispositivos Portáteis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




