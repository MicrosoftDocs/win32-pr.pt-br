---
description: O método seterrovalue adiciona um novo valor HRESULT (erro de tipo VT \_ ) ou substitui um existente.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Método IPortableDeviceValues:: seterrovalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 41bb9a6d8f2878b9bcfac6584c39fd55153ecae8a539c7f8886a5d0eb90d1bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026784"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>Método IPortableDeviceValues:: SetError

O método **Seterrovalue** adiciona um novo valor **HRESULT** (erro de tipo VT \_ ) ou substitui um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

Um **HRESULT** que contém o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: geterrovalue**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




