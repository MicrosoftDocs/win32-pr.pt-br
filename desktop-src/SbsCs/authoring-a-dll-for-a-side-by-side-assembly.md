---
description: Ao criar seus próprios assemblies lado a lado, siga as diretrizes para criar assemblies lado a lado.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Criando DLLs para assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170035"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Criando DLLs para assemblies lado a lado

Ao criar seus próprios assemblies lado a lado, siga as [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md) e criar qualquer DLL usada no assembly de acordo com as seguintes diretrizes:

-   Suas DLLs devem ser projetadas para que várias versões possam ser executadas ao mesmo tempo e no mesmo processo sem interferir umas com as outras. Por exemplo, muitos aplicativos hospedam vários plug-ins que exigem uma versão diferente de um componente. O desenvolvedor que o assembly lado a lado precisa projetar e testar para garantir que várias versões do componente funcionem corretamente quando executadas ao mesmo tempo no mesmo processo.

-   Se você planeja fornecer seu componente como um componente compartilhado em sistemas anteriores ao Windows XP, você precisará continuar a instalar o componente nesses sistemas como um componente compartilhado de instância única. Nesse caso, você precisa garantir que seu componente seja compatível com versões anteriores.

-   Avalie o uso de objetos quando mais de uma versão do assembly for executada no sistema. Determine se versões diferentes do assembly exigem estruturas de dados separadas, como arquivos mapeados de memória, pipes nomeados, mensagens e classes registradas do Windows, memória compartilhada, semáforos, mutexes e drivers de hardware. Todas as estruturas de dados usadas nas versões de assembly devem ser compatíveis com versões anteriores. Decida quais estruturas de dados podem ser usadas nas versões e quais estruturas de dados devem ser privadas para uma versão. Determine se as estruturas de dados compartilhados exigem objetos de sincronização separados, como semáforos e mutexes.

-   Alguns objetos, como classes de janela e Atoms, são nomeados exclusivamente para cada processo. Objetos como classes de janela devem ter controle de versão para cada assembly usando o manifesto. Para objetos como Atoms, use identificadores específicos de versão, a menos que você planeje compartilhar entre versões. Se você usar identificadores específicos de versão, use o número de versão de quatro partes.

-   Não inclua nenhum código de registro automático em qualquer DLL. Uma DLL em um assembly lado a lado não pode ser autoregistrada.

-   Defina todos os nomes específicos de versão em sua DLL com \# instruções de definição. Isso permite que todas as chaves do registro sejam alteradas de um local. Ao liberar uma nova versão do assembly, você só precisa alterar essa \# instrução de definição. Por exemplo:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Armazene quaisquer dados não persistentes no diretório temporário.

-   Não coloque os dados do usuário em locais globais. Manter os dados do aplicativo separados dos dados do usuário.

-   Atribua a todos os arquivos compartilhados uma versão de arquivo que dependa do nome do aplicativo.

-   Atribua todas as mensagens e estruturas de dados usadas em processos uma versão para impedir o compartilhamento entre processos não intencional.

-   Sua DLL não deve depender do compartilhamento entre as versões que podem não existir, como seções de memória compartilhada que não são compartilhadas entre diferentes versões do seu assembly.

-   Se você adicionar uma nova funcionalidade que não segue o contrato de compatibilidade de interface binária da DLL original, deverá atribuir um novo CLSID, ProgId e nome de arquivo. Versões futuras do assembly lado a lado são necessárias para usar esse CLSID, ProgId e nome de arquivo. Isso evita um conflito quando uma versão da DLL que não está lado a lado é registrada em uma versão lado a lado.

-   Se você reutilizar o mesmo CLSID ou ProgId, teste para garantir que o assembly seja compatível com versões anteriores.

-   Inicialize e defina as configurações padrão para o assembly no código do assembly. Não salve as configurações de padrões no registro.

-   Atribua versões a todas as estruturas de dados.

-   Sua DLL deve armazenar o estado do assembly lado a lado, conforme descrito em [armazenamento de estado de criação para assemblies lado a lado](authoring-state-storage-for-side-by-side-assemblies.md).

 

 



