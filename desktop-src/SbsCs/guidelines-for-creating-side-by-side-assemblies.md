---
description: As diretrizes a seguir discutem como criar seus próprios assemblies do COM ou do Win32 lado a lado.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Diretrizes para criar assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8e8fd2bd31a65477b44d3afcf2156d5160a72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090211"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Diretrizes para criar assemblies lado a lado

As diretrizes a seguir discutem como criar seus próprios assemblies do COM ou do Win32 lado a lado. Talvez não seja necessário criar seus próprios assemblies lado a lado se a funcionalidade necessária for fornecida por um dos [assemblies da Microsoft lado a lado com suporte](supported-microsoft-side-by-side-assemblies.md). Nesse caso, use os assemblies fornecidos pela Microsoft e siga os procedimentos para usar assemblies lado a lado no [usando aplicativos isolados e assemblies lado a lado](using-isolated-applications-and-side-by-side-assemblies.md).

Primeiro, considere se o componente faz um candidato adequado para um assembly lado a lado. Para obter mais informações, consulte [se você deve fornecer um componente compartilhado como um assembly lado a lado?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Para criar um assembly lado a lado, siga estas diretrizes:

-   Decida quais recursos incluir no assembly. Tenha em mente que um assembly consiste em um ou mais arquivos que são sempre fornecidos a aplicativos e clientes juntos. O assembly serve como a unidade fundamental usada para nomenclatura, associação, controle de versão, implantação e [configuração padrão](default-configuration.md). Como regra geral, quando não se sabe se dois recursos pertencem ao mesmo assembly, é recomendável que eles sejam criados para entrar em assemblies separados. Normalmente, um assembly lado a lado consiste em uma única DLL.
-   Crie um [manifesto](manifests.md) do assembly para o assembly. O manifesto deve descrever o objeto COM ou as bibliotecas de tipo no assembly. Para obter mais informações sobre o que deve ser criado em um manifesto de assembly, consulte [manifestos de assembly](assembly-manifests.md).
-   Avalie o uso de objetos quando mais de uma versão do assembly for executada no sistema. Determine se versões diferentes do assembly exigem estruturas de dados separadas, como arquivos mapeados de memória, pipes nomeados, mensagens e classes registradas do Windows, memória compartilhada, semáforos, mutexes e drivers de hardware. Quaisquer estruturas de dados usadas nas versões de assembly devem ser versões compatíveis com versões anteriores. Decida quais estruturas de dados podem ser usadas em versões e quais estruturas de dados devem ser privadas para uma versão. Determine se as estruturas de dados compartilhados exigem objetos de sincronização separados, como semáforos e mutexes.
-   Crie sua DLL para funcionar bem como um assembly lado a lado, respeitando as diretrizes de [criação de uma dll para um assembly lado a lado](authoring-a-dll-for-a-side-by-side-assembly.md).
-   Crie um conjunto de arquivos de cabeçalho e funções auxiliares para fornecer uma maneira fácil para as chaves de registro de versão que contêm o estado do assembly. Os assemblies normalmente salvam suas configurações de estado nas chaves do registro. As configurações do registro devem ser gravadas em uma base de versão individual para isolar várias versões de assembly que podem ser executadas ao mesmo tempo. Projete seu assembly lado a lado e a DLL para armazenar corretamente e manipular o estado do assembly durante cenários de compartilhamento lado a lado. Siga as diretrizes em [armazenamento de estado de criação para assemblies lado a lado](authoring-state-storage-for-side-by-side-assemblies.md).
-   Os desenvolvedores de aplicativos que usam [assemblies privados](/windows/desktop/Msi/private-assemblies) devem proteger o diretório do aplicativo. Se o aplicativo for instalado usando o [Windows Installer](../msi/windows-installer-portal.md), o diretório do aplicativo poderá ser protegido usando a Tabela LockPermissions. Normalmente, o sistema recebe acesso de leitura, gravação e execução a assemblies privados; todos os outros processos recebem apenas acesso de execução e leitura.
-   Teste o assembly usando cenários com compartilhamento lado a lado para garantir que ele seja um assembly lado a lado válido. A instalação bem-sucedida do assembly não é suficiente para garantir que ele funcionará conforme o esperado.
-   Adote um método para numerar atualizações para seu assembly. Cada assembly é associado a um número de versão de quatro partes. Da esquerda para a direita, as partes principal, secundária, de compilação e de revisão são separadas por pontos. Alterar o número principal ou secundário de um assembly para uma versão incompatível com versões anteriores. Altere somente as partes de Build e de revisão para alterações compatíveis com versões anteriores para o assembly. Por exemplo, um desenvolvedor pode adotar um método de numeração no qual todo o 1.0.0. \* os números de versão referem-se às versões de atualização para o assembly versão 1.0.0.0.

 

 
