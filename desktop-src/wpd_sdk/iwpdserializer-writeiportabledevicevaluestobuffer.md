---
description: O método WriteIPortableDeviceValuesToBuffer serializa uma interface IPortableDeviceValues para uma matriz de bytes alocada pelo chamador.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Método IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766545"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>Método IWpdSerializer:: WriteIPortableDeviceValuesToBuffer

O método **WriteIPortableDeviceValuesToBuffer** serializa uma interface **IPortableDeviceValues** para uma matriz de bytes alocada pelo chamador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwOutputBufferLength* \[ no\]
</dt> <dd>

**DWORD** que especifica o tamanho de *pBuffer*, em bytes.

</dd> <dt>

*pResults* \[ no\]
</dt> <dd>

Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) para serializar.

</dd> <dt>

*pBuffer* \[ fora\]
</dt> <dd>

Ponteiro para um buffer alocado pelo chamador. Para saber o tamanho do buffer necessário, chame **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ fora\]
</dt> <dd>

Ponteiro para um **DWORD** que indica o número de bytes que foi realmente gravado no buffer alocado pelo chamador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                          |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um argumento de ponteiro necessário era **nulo**.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | O buffer fornecido pelo chamador não era grande o suficiente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método copia uma interface **IPortableDeviceValues** em um buffer existente. Se você quiser alocar um novo buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




