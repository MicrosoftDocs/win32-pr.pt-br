---
description: O método GetValue recupera um valor PROPVARIANT especificado por uma chave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: Método IPortableDeviceValues::GetValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cce387bfc08c48547603d8b30a3952952f1e2decf70e06986ea4fb477fe4fdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843028"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>Método IPortableDeviceValues::GetValue

O **método GetValue** recupera um **valor PROPVARIANT** especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
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

Ponteiro para o valor **PROPVARIANT** recuperado. O chamador deve liberar a memória chamando **PropVariantClear** quando terminar com ela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Quando o VARTYPE para *pValue* for VT VECTOR ou \_ VT \_ UI1, não há suporte para a recuperação de um buffer **NULL** ou de tamanho zero. Por exemplo, nem pValue.caub.pElems = **NULL** nem pValue.caub.cElems = 0 são permitidos.

Esse método pode ser usado para recuperar um valor de qualquer tipo da coleção. No entanto, se você sabe o tipo de valor com antecedência, use um dos métodos de recuperação especializados dessa interface para evitar a sobrecarga de trabalhar diretamente com valores PROPVARIANT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues::SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




