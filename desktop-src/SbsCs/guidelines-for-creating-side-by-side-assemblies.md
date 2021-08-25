---
description: As diretrizes a seguir discutem como fazer seus próprios assemblies COM ou Win32 lado a lado.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Diretrizes para criar assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885246"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Diretrizes para criar assemblies lado a lado

As diretrizes a seguir discutem como fazer seus próprios assemblies COM ou Win32 lado a lado. Talvez você não precise criar seus próprios assemblies lado a lado se a funcionalidade necessária for fornecida por um dos assemblies lado a [lado da Microsoft com suporte.](supported-microsoft-side-by-side-assemblies.md) Nesse caso, use os assemblies fornecidos pela Microsoft e siga os procedimentos para usar assemblies lado a lado em Usando aplicativos isolados e assemblies lado [a lado.](using-isolated-applications-and-side-by-side-assemblies.md)

Primeiro, considere se o componente é um candidato adequado para um assembly lado a lado. Para obter mais informações, [consulte Você deve fornecer um componente compartilhado como um assembly lado a lado?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Para criar um assembly lado a lado, siga estas diretrizes:

-   Decida quais recursos incluir no assembly. Tenha em mente que um assembly consiste em um ou mais arquivos que sempre são fornecidos para aplicativos e clientes juntos. O assembly serve como a unidade fundamental usada para nomeação, associação, versão, implantação e [configuração padrão.](default-configuration.md) Como regra geral, quando não há certeza de se dois recursos pertencem ao mesmo assembly, é recomendável que eles sejam autorados para entrar em assemblies separados. Normalmente, um assembly lado a lado consiste em uma única DLL.
-   Crie um manifesto [do assembly](manifests.md) para o assembly. O manifesto deve descrever as bibliotecas de tipo ou objeto COM no assembly. Para obter mais informações sobre o que deve ser feito em um manifesto do assembly, consulte [manifestos de assembly](assembly-manifests.md).
-   Avalie o uso de objetos quando mais de uma versão do assembly for executado no sistema. Determine se diferentes versões do assembly exigem estruturas de dados separadas, como arquivos mapeados em memória, pipes nomeados, mensagens e classes Windows registradas, memória compartilhada, semáforos, mutexes e drivers de hardware. Todas as estruturas de dados usadas em versões de assembly devem ser versões compatíveis com versões anteriores. Decida quais estruturas de dados podem ser usadas em versões e quais estruturas de dados devem ser privadas para uma versão. Determine se as estruturas de dados compartilhadas exigem objetos de sincronização separados, como semáforos e mutexes.
-   Autor de sua DLL para funcionar bem como um assembly lado a lado, aderindo às diretrizes em Como autor de uma DLL para um assembly lado [a lado.](authoring-a-dll-for-a-side-by-side-assembly.md)
-   Criar um conjunto de arquivos de header e funções auxiliares para fornecer uma maneira fácil de versão das chaves do Registro que contêm o estado do assembly. Os assemblies normalmente salvam suas configurações de estado em chaves do Registro. As configurações do Registro devem ser escritas em uma base de versão individual para isolar várias versões de assembly que podem ser executados ao mesmo tempo. Projete o assembly lado a lado e a DLL para armazenar e manipular corretamente o estado do assembly durante cenários de compartilhamento lado a lado. Siga as diretrizes em [Estado de Armazenamento para assemblies](authoring-state-storage-for-side-by-side-assemblies.md)lado a lado.
-   Os desenvolvedores de aplicativos que usam [assemblies privados](/windows/desktop/Msi/private-assemblies) devem proteger o diretório do aplicativo. Se o aplicativo for instalado usando o [Windows ,](../msi/windows-installer-portal.md)o diretório do aplicativo poderá ser protegido usando a tabela LockPermissions. Normalmente, o sistema recebe acesso de leitura, gravação e execução a assemblies privados; todos os outros processos só receberão acesso de execução e leitura.
-   Teste o assembly usando cenários com compartilhamento lado a lado para garantir que ele seja um assembly lado a lado válido. A instalação bem-sucedida do assembly não é suficiente para garantir que ele funcionará conforme o esperado.
-   Adote um método para numerar atualizações para o assembly. Cada assembly está associado a um número de versão de quatro partes. Da esquerda para a direita, as partes principais, secundárias, de build e de revisão são separadas por períodos. Altere o número principal ou secundário de um assembly para uma versão incompatível com versões anteriores. Altere somente as partes de build e revisão para alterações compatíveis com versões anteriores no assembly. Por exemplo, um desenvolvedor pode adotar um método de numeração no qual todos os 1.0.0. \* os números de versão referem-se às versões de atualização do assembly versão 1.0.0.0.

 

 
