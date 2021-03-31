---
description: Para forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM, crie o pacote de instalação do aplicativo para especificar uma relação de componentes isolados entre o servidor COM e o cliente.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Instalando um componente COM em um local privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827471"
---
# <a name="installing-a-com-component-to-a-private-location"></a>Instalando um componente COM em um local privado

Para forçar um aplicativo de cliente COM sempre usar a mesma cópia de um servidor COM, crie o pacote de instalação do aplicativo para especificar uma relação de [componentes isolados](isolated-components.md) entre o servidor com e o cliente. Isso instala uma cópia privada do componente COM-Server em um local usado exclusivamente pelo aplicativo cliente. Faça o seguinte ao criar o pacote:

-   Coloque a DLL do servidor COM e o cliente. exe em componentes separados.
-   Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente com-Client na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente. Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.
-   Defina o bit msidbComponentAttributesSharedDllRefCount no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado. O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.

 

 



