---
description: Um administrador pode forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM em um pacote existente&\# 8212; sem afetar outros aplicativos&\# 8212; especificando uma relação de componentes isolados entre o servidor e o cliente.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Tornar um componente não-COM em um pacote particular existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0082d89ca6e921213bb462d1b858154419bef416ffa263b8b63ca6d98660fe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945605"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a>Tornar um componente não-COM em um pacote particular existente

Um administrador pode forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM em um pacote existente, sem afetar outros aplicativos, especificando uma relação de [componentes isolados](isolated-components.md) entre o servidor e o cliente. Isso instala uma cópia privada do componente de servidor em um local usado exclusivamente pelo aplicativo cliente. O administrador precisa usar transformações ou uma ferramenta de criação de pacote para fazer o seguinte:

-   Coloque a DLL do servidor e o cliente do .exe em componentes separados.
-   Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente cliente na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente. Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.
-   Defina o bit **msidbComponentAttributesSharedDllRefCount** no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado. O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.

 

 



