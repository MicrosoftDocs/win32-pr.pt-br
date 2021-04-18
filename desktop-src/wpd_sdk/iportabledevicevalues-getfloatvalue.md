---
description: O método getfloatvalue recupera um valor FLOAT (tipo VT \_ R4) especificado por uma chave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Método IPortableDeviceValues:: getfloatvalue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752139"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>Método IPortableDeviceValues:: getfloatvalue

O método **Getfloatvalue** recupera um valor **float** (tipo VT \_ R4) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

Ponteiro para o valor **float** recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                             | Descrição                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>    | A propriedade especificada pela *chave* não é um tipo **float** .<br/>  |
| <dl> <dt>**ID de prop. de E \_ \_ \_ sem suporte**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: setfloatvalue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




