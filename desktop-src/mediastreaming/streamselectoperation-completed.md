---
title: Propriedade StreamSelectOperation. Completed
description: Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo SelectBestStreamAsync é concluída.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- API de streaming de mídia de propriedade concluída
- API de streaming de mídia de propriedade concluída, interface StreamSelectOperation
- API de streaming de mídia da interface StreamSelectOperation, Propriedade Completed
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105812279"
---
# <a name="streamselectoperationcompleted-property"></a>Propriedade StreamSelectOperation. Completed

Obtém ou define um manipulador de eventos que é invocado quando a operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) é concluída.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Valor da propriedade

O manipulador de eventos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 