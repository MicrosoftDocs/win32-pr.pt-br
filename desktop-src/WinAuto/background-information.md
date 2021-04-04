---
title: Informações gerais
description: O componente do Microsoft Acessibilidade Ativa, oleacc.dll, cria objetos de proxy que implementam o IAccessible em nome de controles padrão do Windows.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084047"
---
# <a name="background-information"></a>Informações gerais

O componente do Microsoft Acessibilidade Ativa, oleacc.dll, cria objetos de proxy que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) em nome de controles padrão do Windows. Como esses proxies usam mensagens padrão do Windows e APIs específicas de controle para coletar informações sobre cada controle, não havia nenhum mecanismo direto para personalizar as informações que esses proxies expõem por meio do **IAccessible**.

No momento, você pode personalizar uma implementação de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente usando as técnicas de subclasse e encapsulamento. No entanto, essas técnicas são entediantes e sujeitas a erros. Na verdade, a maior parte do código escrito para substituir uma ou duas propriedades está preocupada com a implementação de subclasse e quebra automática; apenas uma pequena fração executa a tarefa real de substituir informações. A anotação dinâmica melhora a situação fornecendo recursos semelhantes sem exigir que você escreva o código de subclasse ou encapsulamento. Em vez disso, você pode se concentrar em fornecer código que forneça as informações corretas. A anotação dinâmica permite que os desenvolvedores transmitam dicas e outras informações úteis para OLEACC para personalizar as informações que ele expõe. Esse recurso sozinho reduzirá o custo de suporte ao Microsoft Acessibilidade Ativa e permitirá que os desenvolvedores aprimorem muito a acessibilidade de suas interfaces de usuário.

 

 




