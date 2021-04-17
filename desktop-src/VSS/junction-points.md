---
description: No Windows Vista e no Windows Server 2008, os locais padrão para dados do usuário e dados do sistema foram alterados.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Pontos de junção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797490"
---
# <a name="junction-points"></a>Pontos de junção

No Windows Vista e no Windows Server 2008, os locais padrão para dados do usuário e dados do sistema foram alterados. Por exemplo, os dados do usuário armazenados anteriormente no diretório de documentos e configurações do% SystemDrive% \\ agora são armazenados no diretório% systemdrive% \\ usuários. Para compatibilidade com versões anteriores, os locais antigos têm pontos de junção que apontam para os novos locais. Por exemplo, C: \\ Documents and Settings agora é um ponto de junção que aponta para C: \\ users. Os aplicativos de backup devem ser capazes de fazer backup e restaurar pontos de junção.

Esses pontos de junção podem ser identificados da seguinte maneira:

-   Eles têm o \_ ponto de nova análise de atributo de arquivo, o atributo de \_ \_ arquivo \_ \_ oculto e os atributos de arquivo do sistema de atributo de arquivo \_ \_ definidos.
-   Eles também têm suas ACLs (listas de controle de acesso) definidas para negar acesso de leitura a todos.

Os aplicativos que chamam um caminho específico podem atravessar esses pontos de junção se tiverem as permissões necessárias. No entanto, as tentativas de enumerar o conteúdo dos pontos de junção resultarão em falhas. É importante que os aplicativos de backup não percorram esses pontos de junção ou tentem fazer backup de dados sob eles, por dois motivos:

-   Isso pode fazer com que o aplicativo de backup faça backup dos mesmos dados mais de uma vez.
-   Ele também pode levar a ciclos (referências circulares).

## <a name="per-user-junctions-and-system-junctions"></a>Junções de Per-User e junções de sistema

Os pontos de junção usados para fornecer a virtualização de arquivo e registro no Windows Vista e no Windows Server 2008 podem ser divididos em duas classes: junções por usuário e junções de sistema.

As junções por usuário são criadas dentro de cada perfil de usuário individual para fornecer compatibilidade com versões anteriores para aplicativos de usuário. O ponto de junção em C: \\ Users \\ *username* \\ My Documents que aponta para C: \\ Users \\ *username* \\ Documents é um exemplo de uma junção por usuário. As junções por usuário são criadas pelo serviço de perfil quando o perfil do usuário é criado.

As outras junções são junções de sistema que não residem no diretório Users \\ *username* . Exemplos de junções de sistema incluem:

-   Documentos e configurações
-   Junções dentro de todos os usuários, públicos e perfis de usuário padrão

As junções do sistema são criadas por userenv.dll quando ele é invocado pelo Windows Welcome (também chamado de máquina de experiência mOOBE).

> [!Note]  
> Se o usuário alterar o idioma do sistema para um idioma diferente do inglês, os pontos de junção por usuário e sistema serão criados com nomes localizados.

 

 

 



