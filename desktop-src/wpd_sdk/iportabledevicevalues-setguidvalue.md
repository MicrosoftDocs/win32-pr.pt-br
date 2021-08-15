---
description: O método SetGuidValue adiciona um novo valor GUID (tipo CLSID VT) ou substitui \_ um existente.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: Método IPortableDeviceValues::SetGuidValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de2554422ca9df16a1a1df98a5f4888e4914909885c6661818b0692b33b66763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963585"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a>Método IPortableDeviceValues::SetGuidValue

O **método SetGuidValue** adiciona um novo **valor GUID** (tipo CLSID VT) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ Em\]
</dt> <dd>

Uma **REFPROPERTYKEY** que especifica o item a ser criado ou substituido.

</dd> <dt>

*Valor* \[ Em\]
</dt> <dd>

Um **REFGUID** que contém o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro *key,* ele substituirá o valor existente sem nenhum aviso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Adicionando um recurso a um objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




