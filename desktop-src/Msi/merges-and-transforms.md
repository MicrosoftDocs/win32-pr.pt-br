---
description: O Windows instalador mantém todas as informações sobre a instalação em um banco de dados relacional. Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclações.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Mesclagem e transformação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9779cd901df349b80dba84f056104c316810f8a3f67b19cdd4622dd68480ce1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012974"
---
# <a name="merges-and-transforms"></a>Mesclagem e transformação

O Windows instalador mantém todas as informações sobre a instalação em um banco de dados relacional. Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclações.

## <a name="transforms"></a>Transformações

Uma [transformação de banco de](database-transforms.md) dados adiciona ou substitui elementos no banco de dados original. Por exemplo, uma transformação pode alterar todo o texto na interface do usuário de um aplicativo de francês para inglês.

Os principais usos para as transformação incluem:

-   Personalização de pacotes de instalação base para grupos específicos de usuários.

    As transformação podem ser usadas para encapsular as várias personalizações de um único pacote base que são exigidas por diferentes grupos de usuários. Por exemplo, isso é útil em organizações em que os departamentos de suporte financeiro e de equipe exigem instalações diferentes de um produto específico. O pacote base de um produto pode estar disponível para todos em um ponto de instalação administrativa com personalizações apropriadas distribuídas para cada grupo de usuários separadamente.

-   Sincronização de aplicativos entre idiomas.

    As transformares são úteis para manter os pacotes de autor em locais amplamente separados sincronizados durante a comação. Por exemplo, se uma atualização for desenvolvida pela primeira vez para uma versão em inglês de um aplicativo que existe em inglês e francês, uma transformação poderá ser aplicada à versão atualizada em inglês que a converte em uma versão em francês atualizada.

    Várias transformares podem ser aplicadas a um pacote base e, em seguida, aplicadas em tempo real durante a instalação. Isso estende os recursos do instalador para criar pacotes personalizados e fornece um mecanismo para atribuir com eficiência as instalações mais apropriadas a diferentes grupos de usuários.

-   Aplicações de aplicação de patch.

    As transformação podem ser usadas para aplicar uma correção secundária a um aplicativo que não garante uma atualização importante. Para obter mais informações sobre patches, consulte [Pacotes de patch](patch-packages.md).

## <a name="merges"></a>Mesclagens

Uma mesclagem combina dois bancos de dados em um banco de dados e adiciona, em vez de substituir, informações. Se as mesmas informações existirem em ambos os bancos de dados, ocorrerá um conflito de mesclagem. As mesclagem são úteis para as equipes de desenvolvimento porque permitem que um aplicativo grande seja dividido em partes que podem ser recombinadas posteriormente. Por exemplo, os elementos de banco de dados para a instalação de um novo componente podem ser desenvolvidos separadamente e mesclados posteriormente no banco de dados de instalação principal. Para obter mais informações, consulte [Mesclar módulos](merge-modules.md).

Uma equipe de desenvolvimento pode aplicar uma operação de mesclagem da seguinte maneira:

1.  Separe em grupos e trabalhe simultaneamente em diferentes componentes de um aplicativo grande.
2.  Em seguida, cada grupo de desenvolvimento popula um banco de dados com informações de instalação para seu próprio componente, sem se preocupar com os outros componentes do aplicativo.
3.  Após a conclusão do desenvolvimento de um componente, o banco de dados desse componente pode ser mesclado ao banco de dados de instalação principal para todo o aplicativo.

 

 



