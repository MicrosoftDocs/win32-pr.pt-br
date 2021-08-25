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
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704516"
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

## <a name="return-value"></a>Valor retornado

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

 

 




