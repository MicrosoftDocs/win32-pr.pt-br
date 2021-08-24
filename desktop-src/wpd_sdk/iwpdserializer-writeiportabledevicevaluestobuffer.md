---
description: O método WriteIPortableDeviceValuesToBuffer serializa uma interface IPortableDeviceValues para uma matriz de byte alocada pelo chamador.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: Método IWpdSerializer::WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes.h)
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
ms.openlocfilehash: db86953e2e08c0a66f6e497c1fcd2350cc726be8852803cf8f4d64bfff523500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657736"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>Método IWpdSerializer::WriteIPortableDeviceValuesToBuffer

O **método WriteIPortableDeviceValuesToBuffer** serializa uma interface **IPortableDeviceValues** para uma matriz de byte alocada pelo chamador.

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

*dwOutputBufferLength* \[ Em\]
</dt> <dd>

**DWORD** que especifica o tamanho de *pBuffer*, em bytes.

</dd> <dt>

*pResults* \[ Em\]
</dt> <dd>

Ponteiro para uma [**interface IPortableDeviceValues**](iportabledevicevalues.md) a ser serializado.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Ponteiro para um buffer alocado pelo chamador. Para saber o tamanho do buffer necessário, chame **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ out\]
</dt> <dd>

Ponteiro para um **DWORD** que indica o número de bytes que realmente foram gravados no buffer alocado pelo chamador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                          |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um argumento de ponteiro necessário era **NULL.**<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | O buffer fornecido pelo chamador não era grande o suficiente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método copia uma interface **IPortableDeviceValues** em um buffer existente. Se você quiser alocar um novo buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWpdSerializer Interface**](iwpdserializer.md)
</dt> </dl>

 

 




