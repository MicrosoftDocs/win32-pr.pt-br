---
description: O método SetKeyValue adiciona um novo valor REFPROPERTYKEY (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Método IPortableDeviceValues:: SetKeyValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 850c9752d83e95aa6d602aec5a8d44fa43deb83728d0bc0c3130c30e04151a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584296"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a>Método IPortableDeviceValues:: SetKeyValue

O método **SetKeyValue** adiciona um novo valor **REFPROPERTYKEY** (tipo VT \_ desconhecido) ou substitui um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
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

Um **REFPROPERTYKEY** que especifica o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Adicionando um recurso a um objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetKeyValue**](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




