---
description: Em determinados casos, os autores podem decidir que precisam quebrar as regras para criar componentes, conforme discutido em organizando aplicativos em componentes e alterando o código do componente.
ms.assetid: 487b6a00-77eb-4c51-8e32-46bcd4493df8
title: O que acontece se as regras de componente forem interrompidas?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f61a0a819856c5014aa70acfaeb46be5043e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782318"
---
# <a name="what-happens-if-the-component-rules-are-broken"></a>O que acontece se as regras de componente forem interrompidas?

Em determinados casos, os autores podem decidir que precisam quebrar as regras para criar componentes, conforme discutido em [organizando aplicativos em componentes](organizing-applications-into-components.md) e [alterando o código do componente](changing-the-component-code.md). Os autores precisam estar cientes das possíveis consequências de fazer isso e devem garantir que seus componentes nunca sejam instalados, onde possam danificar outros aplicativos ou componentes no sistema do usuário.

A lista a seguir descreve as maneiras pelas quais os autores, às vezes, violam as regras de componente recomendadas e as conseqüências possíveis.

Um autor adiciona recursos a um componente sem alterar o código do componente.

-   Os produtos instalados com o componente antigo não têm informações sobre os recursos adicionados no banco de dados de instalação.
-   Se um novo produto que tem os recursos adicionados e um produto antigo estiver instalado no mesmo computador, os recursos poderão ser deixados para trás se o novo produto for desinstalado primeiro.
-   Um produto antigo sem os recursos adicionados não pode reparar a versão mais recente do componente. A reinstalação do produto antigo não restaura os recursos adicionados.

Um autor remove recursos de um componente sem alterar o código do componente.

-   Os produtos instalados com o novo componente não têm informações sobre os recursos removidos no banco de dados de instalação.
-   Se um produto antigo, tiver as informações de recurso e um novo produto estiver instalado no mesmo computador, os recursos poderão ser deixados para trás se o produto antigo for desinstalado primeiro.
-   Um novo produto com os recursos removidos não pode reparar a versão mais antiga do produto. A reinstalação do novo produto não restaura os recursos removidos.

Um autor inclui um arquivo que é incompatível com as versões anteriores sem alterar o código do componente.

Se um arquivo incompatível estiver incluído em um componente sem alterar o código do componente, o [controle de versão de arquivo padrão](default-file-versioning.md) fará com que o instalador substitua o arquivo original pelo arquivo mais recente incompatível. Isso pode danificar os produtos antigos que precisam do arquivo original. Ele também pode impedir que o instalador repare o produto antigo porque a versão do arquivo de caminho chave do componente determina a versão do componente. Se uma versão mais recente do arquivo de caminho de chave já estiver instalada, o instalador não instalará uma versão mais antiga do componente. Para obter mais informações, consulte [regras de controle de versão de arquivo](file-versioning-rules.md). Nesse caso, o novo produto deve ser removido antes que o produto antigo possa ser reinstalado.

-   O [controle de versão de arquivo padrão](default-file-versioning.md) faz com que o instalador substitua o arquivo original pelo arquivo mais recente incompatível.
-   Os produtos antigos que precisam do arquivo original estão danificados.
-   Ele também pode impedir que o instalador repare o produto antigo porque a versão do arquivo de caminho chave do componente determina a versão do componente. Se uma versão mais recente do arquivo de caminho de chave já estiver instalada, o instalador não instalará a versão mais antiga do componente. Para obter mais informações, consulte [regras de controle de versão de arquivo](file-versioning-rules.md). Nesse caso, o novo produto deve ser removido antes que o produto antigo possa ser reinstalado.

Um autor inclui o mesmo recurso em dois componentes diferentes.

Se dois componentes tiverem um recurso sob o mesmo nome e local e os dois componentes estiverem instalados na mesma pasta, a remoção de um dos componentes removerá o recurso comum, o que danificará o componente restante.

-   A desinstalação de qualquer componente remove o recurso e quebra o outro componente.
-   O mecanismo de contagem de referências de componente está danificado.

 

 



