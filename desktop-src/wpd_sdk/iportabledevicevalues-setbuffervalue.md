---
description: O método setbuffervalue adiciona um novo valor de BYTE \* (tipo VT \_ vector \| VT \_ UI1) ou substitui um existente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Método IPortableDeviceValues:: setbuffervalue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749343"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>Método IPortableDeviceValues:: setbuffervalue

O método **Setbuffervalue** adiciona um novo valor de **byte** \* (tipo VT \_ vector \| VT \_ UI1) ou substitui um existente.

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

*chave* \[ no\]
</dt> <dd>

Um **REFPROPERTYKEY** que especifica o item a ser criado ou substituído.

</dd> <dt>

*valores* \[ no\]
</dt> <dd>

Um **byte \*** que contém os dados a serem gravados no item. Os dados de buffer enviados são copiados para a interface, para que o chamador possa liberar esse buffer depois de fazer essa chamada.

</dd> <dt>

*cbValue* \[ no\]
</dt> <dd>

O tamanho do valor apontado *por value, em* bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Se um valor existente tiver a mesma chave especificada pelo parâmetro de *chave* , ele substituirá o valor existente sem nenhum aviso. A memória de chave existente é liberada adequadamente.

Não há suporte para a definição de um buffer **nulo** ou de tamanho zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: getbuffervalue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




