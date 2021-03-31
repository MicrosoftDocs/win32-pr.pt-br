---
title: Recurso HTML
description: Define um arquivo HTML.
ms.assetid: d3cf8348-8c10-41d9-a061-cdce0e13abf4
keywords:
- Menus de recursos HTML e outros recursos
topic_type:
- apiref
api_name:
- HTML
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db6477aed5180ae18b99f53f4ebadf9d0ad0c91
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823307"
---
# <a name="html-resource"></a>Recurso HTML

Define um arquivo HTML.

``` syntax
nameID HTML filename
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro sem sinal de 16 bits que identifica o recurso.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

O nome do arquivo HTML. Ele deve ser um caminho completo ou relativo se o arquivo não estiver no diretório de trabalho atual. O caminho deve ser uma cadeia de caracteres entre aspas.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo a seguir define um recurso HTML:

``` syntax
ID_RESPONSE_ERROR_PAGE  HTML "res\\responseerorpage.htm"
```

 

 




