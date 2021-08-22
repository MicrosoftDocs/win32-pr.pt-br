---
description: O método SetBoolValue adiciona um novo valor booliana (tipo BOOL VT) ou substitui \_ um existente.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: Método IPortableDeviceValues::SetBoolValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: a4829d1c7f54042864dc4f54f26a17fcf4b0f84daab9352961d775d97adb45cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026774"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a>Método IPortableDeviceValues::SetBoolValue

O **método SetBoolValue** adiciona um novo valor **booliana** (tipo BOOL VT) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
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

Um **BOOL** que especifica o novo valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro *de* chave, ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBoolValue**](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




