---
description: Determina se um aplicativo e uma cadeia de caracteres de tópico (&\# 0034; AppName \| topicname&\# 0034;) usa a sintaxe correta.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Função NDdeIsValidAppTopicList (Nddeapi. h)
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
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794454"
---
# <a name="nddeisvalidapptopiclist-function"></a>Função NDdeIsValidAppTopicList

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Determina se um aplicativo e uma cadeia de caracteres de tópico ("*AppName* \| *topicname*") usam a sintaxe correta.

## <a name="syntax"></a>Sintaxe


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*targetTopic* \[ no\]
</dt> <dd>

Um ponteiro para a cadeia de caracteres do aplicativo e do tópico a ser validado. Este parâmetro não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o parâmetro *targetTopic* tiver uma sintaxe válida, o valor de retorno será diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

Essa função também é chamada por [**NDdeShareAdd**](nddeshareadd.md) quando cria o compartilhamento DDE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Nomes Unicode e ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) e **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Funções DDE de rede](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




