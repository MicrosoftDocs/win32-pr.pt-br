---
description: O método SetFloatValue adiciona um novo valor FLOAT (tipo VT R4) ou substitui \_ um existente.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: Método IPortableDeviceValues::SetFloatValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 347cf93fe68e989eebb921472d1e81e4d0aa650e92d2c535dfdd93a6d823ed1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657806"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a>Método IPortableDeviceValues::SetFloatValue

O **método SetFloatValue** adiciona um novo valor **FLOAT** (tipo VT R4) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
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

Um **FLOAT** que contém o novo valor.

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

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetFloatValue**](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




