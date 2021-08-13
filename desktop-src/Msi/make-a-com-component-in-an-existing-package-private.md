---
description: Um administrador pode forçar um aplicativo cliente COM a sempre usar a mesma cópia de um servidor COM em um pacote existente&8212; sem afetar outros aplicativos \#&8212; especificando uma relação de componentes isolados entre o servidor COM e o \# cliente.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Tornar um componente COM em um pacote existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5119e2d9417f51bb815fe9c76cd47be496e4c03cab81e4e0ccd2b7c49c7b8b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629027"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Tornar um componente COM em um pacote existente privado

Um administrador pode forçar um aplicativo cliente COM a sempre usar a mesma cópia de um servidor COM [](isolated-components.md) em um pacote existente , sem afetar outros aplicativos, especificando uma relação de componentes isolados entre o servidor COM e o cliente. Isso instala uma cópia privada do componente COM-server em um local usado exclusivamente pelo aplicativo cliente. O administrador precisa usar transformar ou uma ferramenta de autor de pacote para fazer o seguinte:

-   Coloque a DLL do servidor COM e o .exe cliente em componentes separados.
-   Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente COM-client na coluna Componente Compartilhado e o aplicativo cliente na \_ coluna Aplicativo de \_ Componente. Inclua a [ação IsolateComponents nas](isolatecomponents-action.md) tabelas de sequência.
-   De definir o bit **msidbComponentAttributesSharedDllRefCount** no registro da tabela Componente para Componente [](component-table.md) \_ Compartilhado. O instalador requer essa refcount global no local compartilhado para proteger os arquivos compartilhados e o registro em casos em que há compartilhamento com outras tecnologias de instalação.

 

 



