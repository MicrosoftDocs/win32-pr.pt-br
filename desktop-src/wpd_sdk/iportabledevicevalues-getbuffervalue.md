---
description: O método getbuffervalue recupera um valor de matriz de bytes (tipo VT \_ vector \| VT \_ UI1) especificado por uma chave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Método IPortableDeviceValues:: getbuffervalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771481"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>Método IPortableDeviceValues:: getbuffervalue

O método **Getbuffervalue** recupera um valor de **matriz de bytes** (tipo VT \_ vector \| VT \_ UI1) especificado por uma chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
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

Ponteiro para o **valor de byte \* *_ recuperado. O chamador é responsável por liberar a memória chamando _* CoTaskMemFree**.

</dd> <dt>

*pcbValue* \[ fora\]
</dt> <dd>

Ponteiro para o tamanho de *ppValue*, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                                            | Descrição                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | A propriedade especificada pela *chave* não é um tipo de **byte** \* .<br/> |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ não \_ encontrado)**</dt> </dl> | A propriedade especificada pela *chave* não está na coleção.<br/> |



 

## <a name="remarks"></a>Comentários

Não há suporte para a recuperação de um buffer **nulo** ou de um buffer de tamanho zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: setbuffervalue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




