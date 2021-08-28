---
description: O método SetValue adiciona um novo valor PROPVARIANT ou substitui um existente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Método IPortableDeviceValues:: SetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f6af975b2876a177207df4f57bfe1f76d78a4b7239ce6d9c4cfcab52f0cf9042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055036"
---
# <a name="iportabledevicevaluessetvalue-method"></a>Método IPortableDeviceValues:: SetValue

O método **SetValue** adiciona um novo valor **PROPVARIANT** ou substitui um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.

</dd> <dt>

*valores* \[ no\]
</dt> <dd>

Um **PROPVARIANT** que especifica o novo valor. O SDK copia o valor para que o chamador possa liberar a variável local chamando **PropVariantClear** depois de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para definir um buffer **nulo** ou de tamanho zero. Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.

Esse método pode ser usado para recuperar um valor de qualquer tipo da coleção. No entanto, se você souber o tipo de valor com antecedência, use um dos métodos **set...** especializados dessa interface para evitar a sobrecarga de trabalhar com valores de PROPVARIANT diretamente.

Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues:: RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




