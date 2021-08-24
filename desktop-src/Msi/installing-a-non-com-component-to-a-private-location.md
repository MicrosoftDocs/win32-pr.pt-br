---
description: Para forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM, crie o pacote de instalação do aplicativo para especificar uma relação de componentes isolados entre o servidor e o cliente.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Instalando um componente não COM em um local privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d8b835b5b0d734caaf5b5b20d062cd540510776371f72e7019efdc72e12cf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119295436"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a>Instalando um componente não COM em um local privado

Para forçar um aplicativo cliente a sempre usar a mesma cópia de um servidor não COM, crie o pacote de instalação do aplicativo para especificar uma relação de [componentes isolados](isolated-components.md) entre o servidor e o cliente. Isso instala uma cópia privada do componente de servidor em um local usado exclusivamente pelo aplicativo cliente. Faça o seguinte ao criar o pacote:

-   Coloque a DLL do servidor e o cliente do .exe em componentes separados.
-   Insira um registro na [tabela IsolatedComponent](isolatedcomponent-table.md) com o componente cliente na \_ coluna compartilhada do componente e o aplicativo cliente na \_ coluna aplicativo do componente. Inclua a [ação IsolateComponents](isolatecomponents-action.md) nas tabelas de sequência.
-   Defina o bit msidbComponentAttributesSharedDllRefCount no registro da [tabela de componentes](component-table.md) para componente \_ compartilhado. O instalador requer esse Refcount global no local compartilhado para proteger os arquivos compartilhados e o registro nos casos em que há compartilhamento com outras tecnologias de instalação.
-   Evite criar um caminho registrado compartilhado entre componentes.

 

 



