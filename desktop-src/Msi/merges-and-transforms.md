---
description: O Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional. Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclagens.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Mesclagens e transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748152"
---
# <a name="merges-and-transforms"></a>Mesclagens e transformações

O Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional. Você pode modificar esse banco de dados e, portanto, a instalação, usando transformações e mesclagens.

## <a name="transforms"></a>Transformações

Uma [transformação de banco de dados](database-transforms.md) adiciona ou substitui elementos no banco de dados original. Por exemplo, uma transformação pode alterar todo o texto na interface do usuário de um aplicativo de francês para inglês.

Os usos primários para transformações incluem:

-   Personalização de pacotes de instalação base para determinados grupos de usuários.

    As transformações podem ser usadas para encapsular as várias personalizações de um único pacote base exigido por diferentes grupos de usuários. Por exemplo, isso é útil em organizações nas quais os departamentos de suporte da equipe e Finanças exigem diferentes instalações de um produto específico. O pacote base de um produto pode estar disponível para todos em um ponto de instalação administrativa com personalizações apropriadas distribuídas para cada grupo de usuários separadamente.

-   Sincronização de aplicativos entre linguagens.

    As transformações são úteis para manter os pacotes criados em locais amplamente separados sincronizados durante a criação. Por exemplo, se uma atualização for desenvolvida primeiro para uma versão em inglês de um aplicativo que existe em inglês e francês, uma transformação poderá ser aplicada à versão em inglês atualizada que a converte em uma versão em francês atualizada.

    Várias transformações podem ser aplicadas a um pacote base e, em seguida, aplicadas imediatamente durante a instalação. Isso estende os recursos do instalador para criar pacotes personalizados e fornece um mecanismo para atribuir com eficiência as instalações mais apropriadas a diferentes grupos de usuários.

-   Aplicação de patches em aplicativos.

    As transformações podem ser usadas para aplicar uma correção secundária a um aplicativo que não garante uma atualização importante. Para obter mais informações sobre patches, consulte [pacotes de patches](patch-packages.md).

## <a name="merges"></a>Mesclagens

Uma mesclagem combina dois bancos de dados em um único e adiciona, em vez de substituir, informações. Se as mesmas informações existirem em ambos os bancos de dados, ocorrerá um conflito de mesclagem. As mesclagens são úteis para as equipes de desenvolvimento porque permitem que um aplicativo grande seja dividido em partes que podem ser recombinadas mais tarde. Por exemplo, os elementos de banco de dados para a instalação de um novo componente podem ser desenvolvidos separadamente e posteriormente mesclados no banco de dados de instalação principal. Para obter mais informações, consulte [Mesclar módulos](merge-modules.md).

Uma equipe de desenvolvimento pode aplicar uma operação de mesclagem da seguinte maneira:

1.  Separe em grupos e trabalhe simultaneamente em diferentes componentes de um aplicativo grande.
2.  Em seguida, cada grupo de desenvolvimento popula um banco de dados com informações de instalação para seu próprio componente, sem se preocupar com os outros componentes do aplicativo.
3.  Após a conclusão do desenvolvimento de um componente, o banco de dados desse componente poderá ser mesclado no banco de dados de instalação principal do aplicativo inteiro.

 

 



