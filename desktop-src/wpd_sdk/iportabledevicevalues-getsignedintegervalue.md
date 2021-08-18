---
description: O método GetSignedIntegerValue recupera um valor longo (tipo VT \_ i4) especificado por uma chave.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'Método IPortableDeviceValues:: GetSignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5b2bab46a7509ce858af9db3c7c4785de5161b64e86c0f3c280fdad00ebe5f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842999"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a>Método IPortableDeviceValues:: GetSignedIntegerValue

O método **GetSignedIntegerValue** recupera um valor **longo** (tipo VT \_ i4) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
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

Ponteiro para o valor **longo** recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada pela *chave* não é um tipo **longo** .<br/>   |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




