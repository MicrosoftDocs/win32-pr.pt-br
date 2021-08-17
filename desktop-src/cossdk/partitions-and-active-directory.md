---
description: Além das partições, que contêm um ou mais aplicativos, o COM+ também inclui conjuntos de partições, que contêm uma ou mais partições.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partições e Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144dde53c6247dcf09dbf9540ce535afb12725822b8e9895f7eb33b569135089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462136"
---
# <a name="partitions-and-active-directory"></a>Partições e Active Directory

Além das partições, que contêm um ou mais *aplicativos,* o COM+ também inclui conjuntos de partições , que contêm uma ou mais partições. Criados no Active Directory, os conjuntos de partições permitem que os usuários em um domínio acessem aplicativos COM+ em todo o domínio. Durante a criação, cada UO (unidade organizacional) ou usuário específico é atribuído, ou mapeado, a um conjunto de partições.

Um único usuário ou UO pode acessar várias partições e seus aplicativos porque há uma correlação um-para-um entre uma identidade de usuário ou UO e um conjunto de partições. Sem um conjunto de partições, um usuário ou UO precisaria de várias identidades de usuário para acessar aplicativos em partições diferentes.

Para disponibilizar aplicativos COM+ para usuários de domínio, um administrador deve executar tarefas no controlador de domínio em que o Active Directory reside e no servidor em que o aplicativo COM+ está instalado.

## <a name="on-the-domain-controller"></a>No controlador de domínio

O administrador primeiro cria uma partição no Active Directory. A criação de uma partição COM+ é feita por meio do uso da ferramenta Usuários e Computadores do Active Directory administrativa ou programaticamente usando a ADSI (Interface de Serviços do Active Directory).

Depois que a partição tiver sido criada no Active Directory, o administrador criará um conjunto de partições. Ao criar um conjunto de partições, o administrador define as partições incluídas nesse conjunto. A criação de um conjunto de partições COM+ é feita por meio do uso da ferramenta Usuários e Computadores do Active Directory administrativa ou programaticamente usando a ADSI (Interface de Serviços do Active Directory).

Por fim, o administrador mapeia usuários de domínio ou unidades organizacionais (OUs) para o conjunto de partições recém-criado. Isso é feito exibindo a  página Propriedades de um usuário, acessando a guia Conjuntos de Partições **COM+** e selecionando um conjunto de partições na caixa de listagem.

## <a name="on-the-com-application-server"></a>No Servidor de Aplicativos COM+

O administrador cria uma nova partição, especificando o mesmo nome de partição e GUID (ID de partição) que a da partição que foi criada no Active Directory no controlador de domínio. Isso é feito usando a pasta **Partições COM+** dentro da ferramenta administrativa dos Serviços de Componentes. Para simplificar essa tarefa, a ferramenta Serviços de Componentes permite que o administrador procure o Active Directory para selecionar a partição desejada e seu GUID.

Quando a partição de domínio tiver sido criada no servidor de aplicativos, a partição padrão de um usuário se tornará a partição padrão do conjunto de partições no Active Directory. Por fim, o administrador pode instalar o aplicativo COM+ na partição recém-criada no servidor de aplicativos.

Para obter mais informações sobre como administrar partições para acesso por usuários de domínio, consulte a ajuda associada à Usuários e Computadores do Active Directory administrativa.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Mapeando identidades de usuário e OUs para conjuntos de partições

Usuários e OUs podem ser mapeados para um conjunto de partições. Ao mapear as OUs para conjuntos de partições, um administrador pode associar vários usuários a um conjunto de partições ao mesmo tempo, em vez de precisar mapear várias identidades de usuário. Uma única identidade de usuário ou UO pode ser mapeada apenas para um conjunto de partições. Em geral, o mapeamento de identidades de usuário ou de OUs para conjuntos de partições faz o seguinte:

-   Garante que os aplicativos estão disponíveis para os usuários apropriados no domínio
-   Ajuda o COM+ a determinar a partição na qual um aplicativo está localizado
-   Estabelece o direito de um usuário de acessar um aplicativo específico

Para associar partições a conjuntos de partições no Active Directory e mapear usuários e OUs para esses conjuntos de partições, os administradores usam as ferramentas administrativas Usuários e Computadores do Active Directory e Serviços de Componentes. Quando uma partição é criada no Active Directory, um administrador precisa configurar localmente essa partição no computador em que o aplicativo COM+ relevante deve ser instalado. Essa configuração local de partições criadas no Active Directory é feita por meio da ferramenta administrativa serviços de componentes.

Se uma identidade de usuário de domínio não for mapeada para um conjunto de partições, o usuário terá acesso pela UO do usuário, que é mapeada para a partição. Se a UO do usuário não for mapeada para um conjunto de partições, mas a próxima UO mais alta na hierarquia for mapeada para esse conjunto de partições, o usuário poderá acessar a partição.

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

 

 



