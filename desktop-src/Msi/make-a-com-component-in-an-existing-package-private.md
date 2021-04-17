---
description: Um administrador pode forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM em um pacote existente&\# 8212; sem afetar outros aplicativos&\# 8212; especificando uma relação de componentes isolados entre o servidor com e o cliente.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Tornar um componente COM em um pacote existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768730"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a>Tornar um componente COM em um pacote existente privado

Um administrador pode forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM em um pacote existente, sem afetar outros aplicativos, especificando uma relação de [componentes isolados](isolated-components.md) entre o servidor com e o cliente. Isso instala uma cópia privada do componente COM-Server em um local usado exclusivamente pelo aplicativo cliente. O administrador precisa usar transformações ou uma ferramenta de criação de pacote para fazer o seguinte:

-   Coloque a DLL do servidor COM e o cliente. exe em componentes separados.
-   Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente com-Client na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente. Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.
-   Defina o bit **msidbComponentAttributesSharedDllRefCount** no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado. O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.

 

 



