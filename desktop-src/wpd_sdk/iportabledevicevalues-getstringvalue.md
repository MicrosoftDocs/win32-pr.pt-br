---
description: O método GetStringValue recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Método IPortableDeviceValues:: GetStringValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813478"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a>Método IPortableDeviceValues:: GetStringValue

O método **GetStringValue** recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Uma chave **REFPROPERTYKEY** que especifica o item a ser recuperado.

</dd> <dt>

*valores* \[ fora\]
</dt> <dd>

Ponteiro para o valor de **LPWSTR** recuperado. O chamador é responsável por chamar **CoTaskMemFree** para liberar a memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada pela *chave* não é um tipo de **LPWSTR** .<br/> |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>  |



 

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

[**IPortableDeviceValues::GetAt**](iportabledevicevalues-getat.md)
</dt> <dt>

[**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de serviço com suporte](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> </dl>

 

 




