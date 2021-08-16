---
description: O método setiunknownvalue adiciona um novo valor IUnknown (tipo VT \_ desconhecido) ou substitui um existente.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'Método IPortableDeviceValues:: setiunknownvalue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c4a7c8a77cfef505b2a507b6281b931eea7f09c4ea1fbc79e651e7f517593799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697047"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a>Método IPortableDeviceValues:: setiunknownvalue

O método **Setiunknownvalue** adiciona um novo valor **IUnknown** (tipo VT \_ desconhecido) ou substitui um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
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

Um ponteiro para uma interface **IUnknown** que especifica o novo valor. O SDK copia uma referência para a interface enviada e chama **AddRef** nela.

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

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: getiunknownvalue**](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




