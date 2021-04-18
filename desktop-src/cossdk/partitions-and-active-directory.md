---
description: Além das partições, que contêm um ou mais aplicativos, o COM+ também inclui conjuntos de partições, que contêm uma ou mais partições.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partições e Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778799"
---
# <a name="partitions-and-active-directory"></a>Partições e Active Directory

Além das partições, que contêm um ou mais aplicativos, o COM+ também inclui *conjuntos* de partições, que contêm uma ou mais partições. Criado em Active Directory, os conjuntos de partições permitem que os usuários em um domínio acessem aplicativos COM+ em todo o domínio. Durante a criação, cada usuário específico ou unidade organizacional (UO) é atribuído ou mapeado para um conjunto de partições.

Um único usuário ou UO pode acessar várias partições e seus aplicativos porque há uma correlação um-para-um entre uma identidade de usuário ou uma unidade organizacional e um conjunto de partições. Sem um conjunto de partições, um usuário ou UO precisaria de várias identidades de usuário para acessar aplicativos em partições diferentes.

Para disponibilizar aplicativos COM+ para usuários de domínio, um administrador deve executar tarefas no controlador de domínio onde Active Directory reside e no servidor em que o aplicativo COM+ está instalado.

## <a name="on-the-domain-controller"></a>No controlador de domínio

O administrador primeiro cria uma partição dentro de Active Directory. A criação de uma partição COM+ é feita por meio do uso da ferramenta administrativa usuários e computadores Active Directory ou programaticamente usando a interface do Active Directory Services (ADSI).

Depois que a partição tiver sido criada dentro do Active Directory, o administrador criará um conjunto de partições. Ao criar um conjunto de partições, o administrador define as partições incluídas nesse conjunto. A criação de um conjunto de partições COM+ é feita por meio do uso da ferramenta administrativa usuários e computadores do Active Directory ou programaticamente usando a interface do Active Directory Services (ADSI).

Por fim, o administrador mapeia usuários de domínio ou UOs (unidades organizacionais) para o conjunto de partições recém-criado. Isso é feito exibindo a página de **Propriedades** de um usuário, acessando a guia **conjuntos de partições com+** e selecionando um conjunto de partições na caixa de listagem.

## <a name="on-the-com-application-server"></a>No servidor de aplicativos COM+

O administrador cria uma nova partição, especificando o mesmo nome de partição e a ID de partição (GUID) que a partição que foi criada dentro de Active Directory no controlador de domínio. Isso é feito usando a pasta **partições com+** na ferramenta administrativa serviços de componentes. Para simplificar essa tarefa, a ferramenta serviços de componentes permite que o administrador procure Active Directory selecione a partição desejada e seu GUID.

Quando a partição de domínio tiver sido criada no servidor de aplicativos, a partição padrão de um usuário se tornará a partição padrão do conjunto de partições no Active Directory. Por fim, o administrador pode instalar o aplicativo COM+ na partição recém-criada no servidor de aplicativos.

Para obter mais informações sobre como administrar partições para acesso por usuários do domínio, consulte a ajuda associada à ferramenta administrativa usuários e computadores do Active Directory.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Mapeando identidades de usuário e UOs para conjuntos de partições

Os usuários e as UOs podem ser mapeados para conjuntos de partições. Mapeando UOs para conjuntos de partições, um administrador pode associar vários usuários a uma partição definida ao mesmo tempo em vez de ter que mapear várias identidades de usuário. Uma única identidade de usuário ou UO só pode ser mapeada para um conjunto de partições. Em geral, o mapeamento de identidades de usuário ou UOs para conjuntos de partições faz o seguinte:

-   Garante que os aplicativos estejam disponíveis para os usuários apropriados no domínio
-   Ajuda COM+ a determinar a partição na qual um aplicativo está localizado
-   Estabelece um direito do usuário para acessar um aplicativo específico

Para associar partições a conjuntos de partições no Active Directory e mapear usuários e UOs para esses conjuntos de partições, os administradores usam o Active Directory usuários e computadores e ferramentas administrativas de serviços de componentes. Quando uma partição é criada dentro do Active Directory, um administrador precisa configurar localmente essa partição no computador em que o aplicativo COM+ relevante deve ser instalado. Essa configuração local de partições criadas dentro de Active Directory é feita por meio da ferramenta administrativa serviços de componentes.

Se uma identidade de usuário de domínio não estiver mapeada para um conjunto de partições, o usuário receberá acesso pela UO do usuário, que é mapeada para a partição. Se a UO do usuário não estiver mapeada para um conjunto de partições, mas a próxima OU mais alta na hierarquia for mapeada para esse conjunto de partições, o usuário poderá acessar a partição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Partições padrão](default-partitions.md)
</dt> <dt>

[Partições locais](local-partitions.md)
</dt> <dt>

[Propriedades da partição](partition-properties.md)
</dt> <dt>

[A partição global](the-global-partition.md)
</dt> </dl>

 

 



