---
description: 'As funções da API do Windows que manipulam caracteres geralmente são implementadas em um dos três formatos:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode na API do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758135"
---
# <a name="unicode-in-the-windows-api"></a>Unicode na API do Windows

As funções da API do Windows que manipulam caracteres geralmente são implementadas em um dos três formatos:

-   Uma versão genérica que pode ser compilada para as páginas de código do Windows ou para o Unicode
-   Uma versão de [página de código do Windows](code-pages.md) com a letra "a" usada para indicar "ANSI"
-   Uma versão [Unicode](unicode.md) com a letra "W" usada para indicar "largo"

Algumas funções mais recentes dão suporte apenas a versões Unicode. Para obter mais informações, consulte [convenções para protótipos de função](conventions-for-function-prototypes.md).

Os tópicos a seguir discutem os tipos de dados Unicode e como eles são usados em funções e mensagens; o uso de recursos, nomes de arquivos e argumentos de linha de comando; e métodos de tradução entre diferentes tipos de cadeias de caracteres.

-   [Tradução automática de mensagens](automatic-message-translation.md)
-   [Conjuntos de caracteres usados em nomes de arquivo](character-sets-used-in-file-names.md)
-   [Argumentos de linha de comando](command-line-arguments.md)
-   [Convenções para protótipos de função](conventions-for-function-prototypes.md)
-   [Funções padrão C](standard-c-functions.md)
-   [Diferenças de função de cadeia de caracteres](string-function-differences.md)
-   [Conversão entre tipos de cadeia de caracteres](translation-between-string-types.md)
-   [Tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Unicode e conjuntos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



