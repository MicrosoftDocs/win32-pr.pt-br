---
description: Este tópico descreve quais bibliotecas são e como elas podem beneficiar usuários e desenvolvedores.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Sobre bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e63aef55513fb36f9a3cbfa71c1b7a79040fd7848468bd1216779cd034132d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049319"
---
# <a name="about-libraries"></a>Sobre bibliotecas

Este tópico descreve quais bibliotecas são e como elas podem beneficiar usuários e desenvolvedores.

As bibliotecas são coleções de pastas definidas pelo usuário. Uma biblioteca controla o local de armazenamento físico de cada pasta, o que alivia o usuário e o software dessa tarefa. Os usuários podem agrupar pastas relacionadas em uma biblioteca, mesmo se essas pastas estiverem armazenadas em diferentes discos rígidos ou em computadores diferentes.

Em uma biblioteca, as pastas e os arquivos aparecem para o usuário como uma única coleção e, usando a API da biblioteca do Shell, o conteúdo da biblioteca também pode parecer estar em um único local para um programa.

Em uma biblioteca, o conteúdo, como documentos, fotos, vídeos ou músicas de um usuário, pode ser classificado e exibido conforme o usuário desejar e não simplesmente como o sistema de arquivos exige. Por exemplo, os usuários podem organizar o conteúdo de uma biblioteca usando as propriedades dos itens na biblioteca para que os itens relacionados sejam classificados juntos mesmo se estiverem armazenados em pastas diferentes.

![captura de tela da interface do usuário das bibliotecas](images/libraries-whatare.png)

Neste tópico:

-   [Benefícios da biblioteca](#library-benefits)
    -   [Benefícios do usuário](#user-benefits)
    -   [Benefícios para o desenvolvedor](#developer-benefits)
-   [Gerenciando pastas em bibliotecas](#managing-folders-in-libraries)
-   [Tópicos relacionados](#related-topics)

## <a name="library-benefits"></a>Benefícios da biblioteca

Esta seção descreve alguns dos benefícios das bibliotecas da perspectiva do usuário final e da perspectiva do desenvolvedor do programa.

### <a name="user-benefits"></a>Benefícios do usuário

A adição de suporte de biblioteca ao seu programa fornece os seguintes benefícios para o usuário:

-   **as bibliotecas fornecem uma interface do usuário consistente no Windows 7**

    as caixas de diálogo arquivo comum dão suporte a bibliotecas e fornecem a mesma experiência de usuário que o Windows Explorer no Windows 7. o suporte a bibliotecas em seu programa ajudará a fornecer uma interação mais direta para o usuário ao usar seu programa no Windows 7.

-   **Os usuários decidem onde armazenar o conteúdo**

    As bibliotecas possibilitam que os usuários controlem onde o conteúdo é armazenado. Ao mesmo tempo, as bibliotecas fornecem padrões razoáveis para os usuários que não desejam gerenciar esse nível de detalhe em seu computador. Os usuários decidem quanto, ou quanto pouco, o controle desejam exercitar onde e como o conteúdo é armazenado e a biblioteca funciona bem de qualquer forma.

### <a name="developer-benefits"></a>Benefícios para o desenvolvedor

Você pode usar bibliotecas em seu programa para fornecer uma interface do usuário mais flexível e conveniente sem precisar adicionar muito código de programa complexo. Algumas das vantagens de adicionar suporte à biblioteca incluem:

-   **Bibliotecas dão suporte ao acesso à biblioteca e ao sistema de arquivos**

    Usando a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), os programas podem fornecer suporte à biblioteca para o usuário, ao mesmo tempo que reduz a complexidade de seu código de gerenciamento de arquivos e pastas. Se o seu programa já usa a API do sistema de arquivos, você pode preservar tanto desse código existente quanto desejar e ainda fornecer suporte de biblioteca ao usuário obtendo as informações necessárias do sistema de arquivos da API da **biblioteca do Shell**.

-   **Notificação de alteração mais simples**

    Tanto o sistema de arquivos quanto a API do Shell podem notificar seu programa quando o conteúdo de uma pasta ou biblioteca monitorada for alterada. No entanto, usando a API do Shell, você pode monitorar todas as pastas na biblioteca com uma única notificação, mesmo que a pasta na biblioteca possa ser armazenada em diferentes unidades ou até mesmo em computadores diferentes.

-   **Bibliotecas usam Propriedades de arquivo**

    Os programas podem usar as propriedades do arquivo para controlar quais arquivos são exibidos durante as operações de abrir e salvar que usam as caixas de diálogo de arquivo comum. Os programas também podem ter acesso às propriedades do arquivo usando as interfaces [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . As caixas de diálogo de arquivo comum também podem ser configuradas para permitir que os usuários atualizem as propriedades associadas ao seu conteúdo.

-   **Os programas podem criar bibliotecas dedicadas**

    Uma nova biblioteca pode ser criada quando as bibliotecas de usuários existentes não atendem às necessidades do programa — por exemplo, se um programa criar um novo tipo de conteúdo de usuário. a nova biblioteca pode ser configurada com um ícone exclusivo que representa seu conteúdo e torna a biblioteca fácil de identificar no Windows Explorer.

## <a name="managing-folders-in-libraries"></a>Gerenciando pastas em bibliotecas

Os usuários podem organizar suas bibliotecas adicionando, movendo ou removendo pastas na biblioteca. Nem todas as pastas, no entanto, dão suporte a toda a funcionalidade que uma biblioteca pode fornecer. muitos recursos de biblioteca exigem acesso rápido às diferentes propriedades da pasta e de seu conteúdo que só estão disponíveis por meio de Windows pesquisa. para fornecer a funcionalidade de biblioteca completa, uma pasta deve ser capaz de ser indexada por Windows pesquisa.

Uma biblioteca não permite que um usuário adicione pastas que não fornecem funcionalidade completa de biblioteca. No entanto, a [**API da biblioteca do Shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pode adicionar essas pastas. Se uma biblioteca contiver uma pasta que não oferece suporte à funcionalidade de biblioteca completa, a biblioteca funcionará em um modo de segurança e fornecerá uma funcionalidade limitada. A tabela a seguir descreve as pastas que oferecem suporte à funcionalidade de biblioteca completa e as que não fazem isso.



| Tipos de pasta que dão suporte à funcionalidade de biblioteca completa                                                               | Tipos de pasta que não dão suporte à funcionalidade de biblioteca completa                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Discos rígidos NTFS e FAT32 fixos e externos.                                                                     | Unidades removíveis, como unidades flash USB ou cartões de memória Secure Digital (SD).               |
| compartilhamentos de arquivos que são indexados por Windows pesquisa como servidores departamentais, Windows 7 ou Windows os PCs domésticos do Vista. | Mídia removível, como mídia de CD-ROM ou DVD.                                                 |
| Compartilhamentos de arquivos que estão disponíveis offline, como uma pasta **meus documentos** redirecionada ou um cache Client-Side.        | Compartilhamentos de rede que não estão disponíveis offline nem remotamente indexados, como unidades NAS.   |
|                                                                                                                    | outras fontes de dados, como o microsoft SharePoint, o microsoft Exchange e o Microsoft OneDrive. |



 

A imagem a seguir mostra a exibição limitada de conteúdo da biblioteca no modo de segurança.

![abrir caixa de diálogo quando as bibliotecas estiverem no modo de segurança](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre bibliotecas](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Links do Shell](./links.md)
</dt> <dt>

[Pastas conhecidas](known-folders.md)
</dt> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> </dl>

 

 
