---
description: 'Windows As funções de API que manipulam caracteres geralmente são implementadas em um dos três formatos:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode na API do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c36e1e292eddd786d4c4bf336f980486f66870deb809587f9c51334f269ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764806"
---
# <a name="unicode-in-the-windows-api"></a>Unicode na API do Windows

Windows As funções de API que manipulam caracteres geralmente são implementadas em um dos três formatos:

-   Uma versão genérica que pode ser compilada para páginas Windows código ou Unicode
-   Uma [Windows de código](code-pages.md) com a letra "A" usada para indicar "ANSI"
-   Uma [versão Unicode](unicode.md) com a letra "W" usada para indicar "wide"

Algumas funções mais recentes suportam apenas versões Unicode. Para obter mais informações, consulte [Convenções para protótipos de função](conventions-for-function-prototypes.md).

Os tópicos a seguir discutem os tipos de dados Unicode e como eles são usados em funções e mensagens; o uso de recursos, nomes de arquivo e argumentos de linha de comando; e métodos de tradução entre diferentes tipos de cadeias de caracteres.

-   [Tradução automática de mensagens](automatic-message-translation.md)
-   [Conjuntos de caracteres usados em nomes de arquivo](character-sets-used-in-file-names.md)
-   [Argumentos de linha de comando](command-line-arguments.md)
-   [Convenções para protótipos de função](conventions-for-function-prototypes.md)
-   [Funções C padrão](standard-c-functions.md)
-   [Diferenças de função de cadeia de caracteres](string-function-differences.md)
-   [Conversão entre tipos de cadeia de caracteres](translation-between-string-types.md)
-   [Tipos de dados do Windows para cadeias de caracteres](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre unicode e conjuntos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



