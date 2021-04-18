---
description: O método GetValue recupera um valor de PROPVARIANT especificado por uma chave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Método IPortableDeviceValues:: GetValue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764203"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>Método IPortableDeviceValues:: GetValue

O método **GetValue** recupera um valor de **PROPVARIANT** especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
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

Ponteiro para o valor **PROPVARIANT** recuperado. O chamador deve liberar a memória chamando **PropVariantClear** quando terminar com ela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para a recuperação de um buffer de tamanho **nulo ou NULL** . Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.

Esse método pode ser usado para recuperar um valor de qualquer tipo da coleção. No entanto, se você souber o tipo de valor com antecedência, use um dos métodos de recuperação especializados dessa interface para evitar a sobrecarga de trabalhar diretamente com valores de PROPVARIANT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues:: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




