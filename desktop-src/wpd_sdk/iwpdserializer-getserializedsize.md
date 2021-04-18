---
description: O método GetSerializedSize calcula o tamanho do buffer necessário para manter uma interface IPortableDeviceValues serializada.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Método IWpdSerializer:: GetSerializedSize (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756518"
---
# <a name="iwpdserializergetserializedsize-method"></a>Método IWpdSerializer:: GetSerializedSize

O método **GetSerializedSize** calcula o tamanho do buffer necessário para manter uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) serializada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSource* \[ no\]
</dt> <dd>

Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) cujo tamanho você deseja solicitar.

</dd> <dt>

*pdwSize* \[ fora\]
</dt> <dd>

Ponteiro para um **DWORD** que indica o tamanho do buffer necessário para serializar *pSource*, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um argumento de ponteiro necessário era **nulo**.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não havia memória suficiente disponível para criar o buffer.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




