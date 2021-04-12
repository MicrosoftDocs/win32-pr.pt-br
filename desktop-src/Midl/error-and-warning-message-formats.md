---
title: Formatos de mensagem de erro e de aviso
description: Lista de mensagens de erro de MIDL e formatos de mensagem de aviso.
ms.assetid: 8eb0f46f-e494-430a-8bb4-b8a21524b62e
keywords:
- MIDL de erros, formatos de mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42552b8106b72d82b2b13b69a7cba7ac2e99e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364395"
---
# <a name="error-and-warning-message-formats"></a>Formatos de mensagem de erro e de aviso

Os erros de linha de comando aparecem no seguinte formato:

``` syntax
Command line error : MIDLnnnn: <error text> 
[<additional error information>]
```

O campo informações adicionais de erro fornece informações específicas do contexto, dependendo da mensagem de erro. Por exemplo, quando ocorre um erro de declaração de tipo não resolvido, o campo informações adicionais de erro exibe o nome do tipo que não pôde ser resolvido.

Os avisos de tempo de compilação aparecem no seguinte formato:

``` syntax
<FileName>(line#) : warning MIDLnnnn: 
<warning text>
[optional context information]:
```

Os erros de tempo de compilação aparecem no seguinte formato:

``` syntax
<FileName>(line#) : error MIDLnnnn: 
<error text>
[optional context information] :
```

Informações de contexto opcionais referem-se ao contexto no qual ocorreu o erro. Ele é gerado quando o compilador MIDL descobre um erro durante a análise semântica de assinaturas de tipo e de procedimento. O compilador MIDL relata essas informações para ajudá-lo a encontrar o erro no arquivo IDL rapidamente.

As mensagens de erro do sistema aparecem no seguinte formato:

``` syntax
<FileName>(line#) : MIDL error 0xnnnn: 
"Unexpected internal compiler problem. Try to find a workaround."
```

Essa mensagem é gerada por um erro que era inesperado. O número de erro hexadecimal é um identificador de erro de sistema do Windows XP, Windows 2000, Windows NT, Windows 98 ou Windows 95. Você pode encontrar informações adicionais em Winerror. h ou Ntstatus. h. Para obter mais informações sobre como solucionar as condições que causaram esse erro, consulte o texto de erro para o [erro do compilador](compiler-errors.md) MIDL9008.

 

 




