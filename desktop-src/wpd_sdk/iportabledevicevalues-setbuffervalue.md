---
description: O método SetBufferValue adiciona um novo valor BYTE \* (tipo VT \_ VECTOR \| VT UI1) ou substitui \_ um existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: Método IPortableDeviceValues::SetBufferValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 25a087c6f2d1e254e225f82ef794915898fbc20c7203fe20315d51f78e9770f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055096"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>Método IPortableDeviceValues::SetBufferValue

O **método SetBufferValue** adiciona um novo valor **BYTE** \* (tipo VT VECTOR \_ \| VT UI1) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ Em\]
</dt> <dd>

Uma **REFPROPERTYKEY** que especifica o item a ser criado ou substituido.

</dd> <dt>

*pValue* \[ Em\]
</dt> <dd>

Um **BYTE \*** que contém os dados a gravar no item. Os dados de buffer enviados são copiados para a interface, para que o chamador possa liberar esse buffer depois de fazer essa chamada.

</dd> <dt>

*cbValue* \[ Em\]
</dt> <dd>

O tamanho do valor apontado por *pValue*, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro *key,* ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

Não há **suporte para** a configuração de um buffer NULL ou de tamanho zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




