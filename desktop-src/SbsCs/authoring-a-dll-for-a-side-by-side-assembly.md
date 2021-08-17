---
description: Ao criar seus próprios assemblies lado a lado, siga as Diretrizes para criar assemblies lado a lado.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Como fazer DLLs para assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb83ba1d788d82e8d4fa7ab5f657170875b5deee6921aec3013406328dc2fcf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142449"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Como fazer DLLs para assemblies lado a lado

Ao criar seus próprios assemblies lado a lado, siga as Diretrizes para criar [assemblies](guidelines-for-creating-side-by-side-assemblies.md) lado a lado e criar quaisquer DLLs usadas no assembly de acordo com as seguintes diretrizes:

-   Suas DLLs devem ser projetadas para que várias versões possam ser executados ao mesmo tempo e no mesmo processo sem interferir entre si. Por exemplo, muitos aplicativos hospedam vários plug-ins que exigem uma versão diferente de um componente. O desenvolvedor do assembly lado a lado precisa projetar e testar para garantir que várias versões do componente funcionem corretamente quando executados ao mesmo tempo no mesmo processo.

-   Se você planeja fornecer seu componente como um componente compartilhado em sistemas anteriores ao Windows XP, precisará continuar a instalar o componente nesses sistemas como um componente compartilhado de instância única. Nesse caso, você precisa garantir que o componente seja compatível com versões anteriores.

-   Avalie o uso de objetos quando mais de uma versão do assembly for executado no sistema. Determine se diferentes versões do assembly exigem estruturas de dados separadas, como arquivos mapeados em memória, pipes nomeados, mensagens e classes Windows registradas, memória compartilhada, semáforos, mutexes e drivers de hardware. Todas as estruturas de dados usadas em versões de assembly devem ser compatíveis com versões anteriores. Decida quais estruturas de dados podem ser usadas em versões e quais estruturas de dados devem ser privadas para uma versão. Determine se as estruturas de dados compartilhadas exigem objetos de sincronização separados, como semáforos e mutexes.

-   Alguns objetos, como classes de janela e Atoms, são nomeados exclusivamente para cada processo. Objetos como classes de janela devem ter a versão de cada assembly usando o manifesto. Para objetos como o Atoms, use identificadores específicos de versão, a menos que você planeje compartilhar entre versões. Se você usar identificadores específicos de versão, use o número de versão de quatro partes.

-   Não inclua nenhum código de auto-registro em nenhuma DLL. Uma DLL em um assembly lado a lado não pode ser auto-registro.

-   Defina todos os nomes específicos da versão em sua DLL com \# instruções define. Isso permite que todas as chaves do Registro sejam alteradas de um local. Ao lançar uma nova versão do assembly, você só precisa alterar essa instrução \# define. Por exemplo:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Armazene todos os dados não persistentes no diretório Temp.

-   Não coloque dados do usuário em locais globais. Mantenha os dados do aplicativo separados dos dados do usuário.

-   Atribua a todos os arquivos compartilhados uma versão de arquivo que dependa do nome do aplicativo.

-   Atribua todas as mensagens e estruturas de dados usadas em processos de uma versão para evitar o compartilhamento não intencional entre processos.

-   Sua DLL não deve depender do compartilhamento entre versões que podem não existir, como seções de memória compartilhada que não são compartilhadas entre diferentes versões do assembly.

-   Se você adicionar uma nova funcionalidade que não segue o contrato de compatibilidade da interface binária da DLL original, deverá atribuir um novo CLSID, ProgId e nome de arquivo. Versões futuras do assembly lado a lado são necessárias para usar essa CLSID, ProgId e o nome do arquivo. Isso impede um conflito quando uma versão da DLL que não está lado a lado é registrada em uma versão lado a lado.

-   Se você reutilizar a mesma CLSID ou ProgId, teste para garantir que o assembly seja compatível com versões anteriores.

-   Inicializar e definir as configurações padrão para o assembly no código do assembly. Não salve as configurações de padrões no Registro.

-   Atribua versões a todas as estruturas de dados.

-   Sua DLL deve armazenar o estado do assembly lado a lado, conforme descrito em Estado de Armazenamento para assemblies lado [a lado.](authoring-state-storage-for-side-by-side-assemblies.md)

 

 



