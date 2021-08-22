---
description: Determina se uma cadeia de caracteres de aplicativo e tópico (&\# 0034; AppName \| TopicName&\# 0034;) usa a sintaxe adequada.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Função NDdeIsValidAppTopicList (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: f7b70d3e33f67c8c0a457f85df91e83e374a3ef4d0f0b1a0af1c5c41ea81c2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611126"
---
# <a name="nddeisvalidapptopiclist-function"></a>Função NDdeIsValidAppTopicList

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

Determina se uma cadeia de caracteres de aplicativo e tópico ("*AppName* \| *TopicName*") usa a sintaxe adequada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*targetTopic* \[ Em\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres do aplicativo e do tópico a ser validado. Esse parâmetro não pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o *parâmetro targetTopic* tiver sintaxe válida, o valor de retorno será diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Essa função também é chamada por [**NDdeShareAdd**](nddeshareadd.md) quando cria o compartilhamento DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nomes Unicode e ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




