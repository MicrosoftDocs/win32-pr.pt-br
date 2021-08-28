---
description: Em determinados casos, os autores podem decidir que precisam quebrar as regras para criar componentes, conforme discutido em Organizando aplicativos em componentes e alterando o código do componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: O que acontece se as regras do componente são interrompidas?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f830fa402da44be992d74adc957d88a19442dcbb51173a87e79fa2266552a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498762"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>O que acontece se as regras do componente são interrompidas?

Em determinados casos, os autores podem decidir que precisam [](organizing-applications-into-components.md) quebrar as regras para criar componentes, conforme discutido em Organizando aplicativos em componentes e [alterando o código do componente](changing-the-component-code.md). Os autores precisam estar cientes das possíveis consequências de fazer isso e, de outra forma, devem garantir que seus componentes nunca sejam instalados onde possam danificar outros aplicativos ou componentes no sistema do usuário.

A lista a seguir descreve maneiras pelas quais os autores, às vezes, quebram as regras de componente recomendadas e as possíveis consequências.

Um autor adiciona recursos a um componente sem alterar o código do componente.

-   Os produtos instalados com o componente antigo não têm informações sobre os recursos adicionados em seu banco de dados de instalação.
-   Se um novo produto que tem os recursos adicionados e um produto antigo estiver instalado no mesmo computador, os recursos poderão ser deixados para trás se o novo produto for desinstalado primeiro.
-   Um produto antigo sem os recursos adicionados não pode reparar a versão mais recente do componente. Reinstalar o produto antigo não restaura os recursos adicionados.

Um autor remove recursos de um componente sem alterar o código do componente.

-   Os produtos instalados com o novo componente não têm informações sobre os recursos removidos no banco de dados de instalação.
-   Se um produto antigo, com as informações do recurso e um novo produto estiver instalado no mesmo computador, os recursos poderão ser deixados para trás se o produto antigo for desinstalado primeiro.
-   Um novo produto com os recursos removidos não pode reparar a versão mais antiga do produto. Reinstalar o novo produto não restaura os recursos removidos.

Um autor inclui um arquivo incompatível com versões anteriores sem alterar o código do componente.

Se um arquivo incompatível for incluído em um componente sem alterar o código do [componente,](default-file-versioning.md) o controle de versão do arquivo padrão faz com que o instalador sobrescreva o arquivo original pelo arquivo incompatível mais recente. Isso pode danificar produtos antigos que precisam do arquivo original. Ele também pode impedir que o instalador repare o produto antigo porque a versão do arquivo de caminho de chave de um componente determina a versão do componente. Se uma versão mais recente do arquivo de caminho da chave já estiver instalada, o instalador não instalará uma versão mais antiga do componente. Para obter mais informações, consulte [Regras de versão de arquivo](file-versioning-rules.md). Nesse caso, o novo produto deve ser removido antes que o produto antigo possa ser reinstalado.

-   [O controle de versão de arquivo](default-file-versioning.md) padrão faz com que o instalador sobrescreva o arquivo original pelo arquivo incompatível mais recente.
-   Produtos antigos que precisam do arquivo original estão danificados.
-   Ele também pode impedir que o instalador repare o produto antigo porque a versão do arquivo de caminho de chave de um componente determina a versão do componente. Se uma versão mais recente do arquivo de caminho da chave já estiver instalada, o instalador não instalará a versão mais antiga do componente. Para obter mais informações, consulte [Regras de versão de arquivo](file-versioning-rules.md). Nesse caso, o novo produto deve ser removido antes que o produto antigo possa ser reinstalado.

Um autor inclui o mesmo recurso em dois componentes diferentes.

Se dois componentes têm um recurso com o mesmo nome e local e ambos os componentes estão instalados na mesma pasta, a remoção de qualquer um dos componentes remove o recurso comum, o que causa danos ao componente restante.

-   A desinstalação de qualquer componente remove o recurso e interrompe o outro componente.
-   O mecanismo de contagem de referência do componente está danificado.

 

 



