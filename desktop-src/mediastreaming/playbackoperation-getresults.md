---
title: Método PlaybackOperation.GetResults
description: Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API de Streaming de Mídia do método GetResults
- API de Streaming de Mídia do método GetResults, interface PlaybackOperation
- API de Streaming de Mídia da interface PlaybackOperation, método GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9bd3c79164a78e7993eb8a58d0d89a64c7ceb31a0c33eaff2e9c1bc352144088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235779"
---
# <a name="playbackoperationgetresults-method"></a>Método PlaybackOperation.GetResults

Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução [**MediaRenderer.**](mediarenderer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

O resultado da operação. Um valor de 0 indica que a operação foi concluída. Outros valores são reservados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

O **método GetResults** normalmente é chamado do manipulador de eventos que foi registrado definindo a [**propriedade**](playbackoperation-completed.md) Completed.

## <a name="see-also"></a>Veja também

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





