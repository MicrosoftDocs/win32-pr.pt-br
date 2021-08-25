---
description: O método SetUnsignedIntegerValue adiciona um novo valor ULONG (tipo VT UI4) ou substitui \_ um existente.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: Método IPortableDeviceValues::SetUnsignedIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9c58569554cf9170788524bdcb233bf42b3318f1e954050bb713711c93337543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928456"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>Método IPortableDeviceValues::SetUnsignedIntegerValue

O **método SetUnsignedIntegerValue** adiciona um novo valor **ULONG** (tipo VT UI4) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
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

Um **ULONG** que especifica o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro *key,* ele substituirá o valor existente sem nenhum aviso.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [**Especificando informações do cliente**](specifying-client-information.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**Especificando informações do cliente**](specifying-client-information.md)
</dt> </dl>

 

 




