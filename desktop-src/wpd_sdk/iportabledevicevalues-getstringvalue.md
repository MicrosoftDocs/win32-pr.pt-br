---
description: O método GetStringValue recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: Método IPortableDeviceValues::GetStringValue (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7d8a9703a359a2de13ec96ff3faf46ea9e49fb1fc467cdade56d799503f1b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806956"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a>Método IPortableDeviceValues::GetStringValue

O **método GetStringValue** recupera um valor de cadeia de caracteres (tipo VT \_ LPWSTR) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ Em\]
</dt> <dd>

Uma **chave REFPROPERTYKEY** que especifica o item a ser recuperado.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Ponteiro para o valor **LPWSTR recuperado.** O chamador é responsável por chamar **CoTaskMemFree** para liberar a memória.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada pela *chave não* é um **tipo LPWSTR.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/>  |



 

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar esse método, consulte Recuperando eventos [de serviço com suporte.](retrieving-supported-events.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetAt**](iportabledevicevalues-getat.md)
</dt> <dt>

[**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de serviço com suporte](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> </dl>

 

 




