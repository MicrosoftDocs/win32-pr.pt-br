---
description: O método GetIPortableDeviceValuesCollectionValue recupera um valor de IPortableDeviceValuesCollection (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Método IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793223"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>Método IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue

O método **GetIPortableDeviceValuesCollectionValue** recupera um valor de **IPORTABLEDEVICEVALUESCOLLECTION** (tipo VT \_ desconhecido) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.

</dd> <dt>

*ppValue* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperada. O chamador é responsável por chamar **Release** na interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada por *chave* não é uma interface **IPortableDeviceValuesCollection** .<br/> |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>                                |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando os recursos de renderização suportados por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[Recuperando os recursos de renderização suportados por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




