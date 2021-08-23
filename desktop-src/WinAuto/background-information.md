---
title: Informações gerais
description: O Microsoft Active Accessibility, oleacc.dll, cria objetos proxy que implementam IAccessible em nome de controles Windows padrão.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d154beb5d824bc722e713346129258c2d294d678a92c1b66d12035ce390f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052954"
---
# <a name="background-information"></a>Informações gerais

O Microsoft Active Accessibility, oleacc.dll, cria objetos proxy que implementam [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) em nome de controles Windows padrão. Como esses proxies usam mensagens Windows padrão e APIs específicas de controle para coletar informações sobre cada controle, não houve nenhum mecanismo direto para personalizar as informações que esses proxies expõem por meio de **IAccessible**.

No momento, você pode personalizar uma implementação [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente usando técnicas de subclasse e de empacotamento. No entanto, essas técnicas são entediantes e propensas a erros. Na verdade, a maioria do código escrito para substituir uma ou duas propriedades se preocupa com a implementação de subclasse e de empacotamento; apenas uma pequena fração executa a tarefa real de substituição de informações. A Anotação Dinâmica melhora a situação fornecendo funcionalidades semelhantes sem exigir que você escreva um código de subclasse ou de empacotamento. Em vez disso, você pode se concentrar em fornecer código que fornece as informações corretas. A Anotação Dinâmica permite que os desenvolvedores passem dicas e outras informações úteis para o OLEACC para personalizar as informações que ela expõe. Essa funcionalidade por si só reduzirá o custo de suporte Microsoft Active Accessibility e permitirá que os desenvolvedores melhorem muito a acessibilidade de suas interfaces do usuário.

 

 




