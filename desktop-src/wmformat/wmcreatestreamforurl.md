---
title: Função WMCreateStreamForURL
description: A função WMCreateStreamForURL é implementada pelo aplicativo para criar um objeto de IStream COM para uma determinada URL.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Formato de mídia do Windows da função WMCreateStreamForURL
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c32302147eeb814c211a77555ab1c9bb3614eddf3d8001015479461e05d40ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653449"
---
# <a name="wmcreatestreamforurl-function"></a>Função WMCreateStreamForURL

A função **WMCreateStreamForURL** é implementada pelo aplicativo para criar um objeto de **IStream** com para uma determinada URL.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszURL* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres largos que contém a URL.

</dd> <dt>

*pfCorrectSource* \[ fora\]
</dt> <dd>

Ponteiro para um sinalizador, true impedirá que o SDK tente outros plug-ins de origem para esta URL.

</dd> <dt>

*PPStream* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro para o objeto **IStream** criado pelo método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem sucedido, ela deverá retornar S \_ OK. Se falhar, ele deve retornar um código de erro **HRESULT** apropriado e \* *PPStream* deve ser definido como **NULL**.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Plug-ins de origem**](source-plug-ins.md)
</dt> </dl>

 

 




