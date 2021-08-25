---
description: O método GetIPortableDeviceValuesValue recupera um valor de IPortableDeviceValues (tipo VT \_ desconhecido) especificado por uma chave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Método IPortableDeviceValues:: GetIPortableDeviceValuesValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: aeec29bf3d9cf18bcf54c885d46d159c21c661a1e886903110952cd3a23c540e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055156"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a>Método IPortableDeviceValues:: GetIPortableDeviceValuesValue

O método **GetIPortableDeviceValuesValue** recupera um valor de **IPORTABLEDEVICEVALUES** (tipo VT \_ desconhecido) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
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

Endereço de uma variável que recebe um ponteiro para a interface [**IPortableDeviceValues**](iportabledevicevalues.md) recuperada. O chamador é responsável por chamar **Release** na interface recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                          |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada por *chave* não é uma interface **IPortableDeviceValues** .<br/> |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>                      |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando eventos de serviço com suporte](retrieving-supported-events.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando os recursos de renderização suportados por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




