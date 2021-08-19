---
description: O método GetFloatValue recupera um valor FLOAT (tipo VT \_ R4) especificado por uma chave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: Método IPortableDeviceValues::GetFloatValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 364b5de9bbf8b3c5bb307b7bbc0e11fc018393c301c0931e065331879ec096fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430819"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>Método IPortableDeviceValues::GetFloatValue

O **método GetFloatValue** recupera um **valor FLOAT** (tipo VT \_ R4) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

Ponteiro para o valor **FLOAT recuperado.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>    | A propriedade especificada pela *chave não* é um **tipo FLOAT.**<br/>  |
| <dl> <dt>**E \_ \_ ID DE PROP \_ SEM SUPORTE**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




