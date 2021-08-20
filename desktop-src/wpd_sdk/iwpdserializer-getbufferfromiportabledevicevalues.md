---
description: O método GetBufferFromIPortableDeviceValues serializa uma interface IPortableDeviceValues enviada para uma matriz de bytes alocada. A matriz de bytes retornada é alocada para o chamador e deve ser liberada pelo chamador usando CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Método IWpdSerializer:: GetBufferFromIPortableDeviceValues (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 10a483331d15c09de8398d11e940453d8f239e2207fdefb82d86fd4bb1460daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843009"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>Método IWpdSerializer:: GetBufferFromIPortableDeviceValues

O método **GetBufferFromIPortableDeviceValues** serializa uma interface **IPortableDeviceValues** enviada para uma matriz de bytes alocada. A matriz de bytes retornada é alocada para o chamador e deve ser liberada pelo chamador usando **CoTaskMemFree**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSource* \[ no\]
</dt> <dd>

Ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) para serializar.

</dd> <dt>

*ppBuffer* \[ fora\]
</dt> <dd>

Ponteiro para um **byte \* *_ que contém os dados serializados. Windows Os dispositivos portáteis alocam essa memória; o chamador deve liberá-lo chamando _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ fora\]
</dt> <dd>

Ponteiro para um **DWORD** que especifica o tamanho do buffer alocado, em bytes.

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

 

 




