---
title: Noções básicas sobre fontes de atributo
description: Noções básicas sobre fontes de atributo
ms.assetid: 83274fea-233d-40dc-b587-99e99ddcd92b
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b7266b75f8f506b1f06e822fbbb40a85d8f2dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636994"
---
# <a name="understanding-attribute-sources"></a>Noções básicas sobre fontes de atributo

Os atributos, ou metadados, que você pode usar vêm de uma variedade de fontes. Este tópico descreve essas fontes, passando de cenários com menos atributos possíveis para aqueles com atributos mais potenciais.

Embora o usuário reproduza um CD ou DVD, você tem acesso a muito poucos metadados sobre o próprio disco ou o conteúdo de mídia do disco. Os discos comerciais normalmente não incluem metadados de atributo.

Se o usuário tiver reproduzido um CD ou DVD enquanto estava conectado à Internet, você poderá ter acesso a mais atributos quando esse disco estiver na unidade de CD ou DVD. Enquanto o Windows Media Player está conectado à Internet e desempenhando um CD ou DVD, o Player recupera os metadados desse disco de um banco de dados online. O Player exibe essas informações no **momento em execução** e em um nó separado na biblioteca. Os atributos não são armazenados no banco de dados de biblioteca, mas são armazenados em cache. Se o cache ainda não tiver sido esvaziado, seu aplicativo terá acesso aos atributos enquanto o disco estiver na unidade.

> [!Note]  
> Os usuários podem optar por não permitir a recuperação de informações de mídia de um banco de dados online. Nesse caso, os únicos atributos disponíveis serão aqueles de um arquivo de mídia digital, aqueles que o usuário inseriu manualmente na biblioteca e os gerados pelo próprio jogador (como os atributos relacionados à frequência com que um item foi reproduzido).

 

Se o usuário reproduzir um arquivo de mídia digital que não é adicionado à biblioteca, você terá acesso aos atributos que estão no arquivo.

Se o usuário reproduzir um arquivo de mídia digital que foi adicionado à biblioteca, você terá acesso aos atributos que são armazenados somente na biblioteca, os atributos que são armazenados somente no arquivo e os atributos que são armazenados na biblioteca e no arquivo.

Os atributos que estão disponíveis para itens de mídia adicionados à biblioteca variam de acordo com o modo como o arquivo de mídia digital de origem foi criado e quais ações o usuário executou desde a adição.

-   O criador de conteúdo pode inserir informações de atributo no arquivo quando ele é criado pela primeira vez. Por exemplo, se você criar e distribuir um arquivo de mídia digital com seu aplicativo, terá controle sobre quais atributos são inseridos originalmente no arquivo.
-   Se o usuário modificar dados de atributo para um item de mídia que tenha sido adicionado à biblioteca, usando o editor de marca avançado ou a interface do usuário da biblioteca, o Windows Media Player adicionará esses dados ao banco de dado da biblioteca. O Player adiciona alguns atributos diretamente ao arquivo porque eles são armazenados apenas no arquivo. Em algum momento determinado, os atributos de leitura/gravação sincronizam com o arquivo para que os atributos armazenados na biblioteca e no arquivo tenham o mesmo valor.
-   Se o usuário copiar uma faixa de um CD usando o Windows Media Player enquanto estiver conectado à Internet, o efeito será praticamente o mesmo que se o usuário tivesse modificado atributos usando o Windows Media Player. Os atributos são adicionados ao banco de dados de biblioteca, extraídos do próprio arquivo e de um banco de dados online. Alguns atributos são armazenados apenas no arquivo. Em algum momento determinado, o banco de dados de biblioteca é sincronizado com o arquivo.
-   Se você escrever código usando o controle do Windows Media Player para alterar o valor de um atributo de leitura/gravação existente em um item de mídia que foi adicionado à biblioteca, o efeito será praticamente o mesmo que se o usuário tivesse modificado o atributo usando o Windows Media Player. O valor é gravado no banco de dados de biblioteca e em algum momento indeterminado que o banco de dados sincroniza com o arquivo.
-   [!Note]  
    > Se você inserir o controle em seu aplicativo, os atributos de arquivo alterados não serão gravados no próprio arquivo de mídia digital até que o usuário execute o Windows Media Player. Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo alterados serão gravados no arquivo de mídia digital logo depois que você fizer as alterações. Em ambos os casos, as alterações ficam imediatamente disponíveis por meio da biblioteca.

     

-   Se você escrever código usando o controle do Windows Media Player para inserir um atributo personalizado em um item de mídia, o atributo e seu valor persistirão somente enquanto o aplicativo tiver uma referência ao objeto de **mídia** . Nem o atributo nem seu valor será armazenado no banco de dados de biblioteca ou no arquivo de mídia digital, se houver um.

A situação mais simples é quando você está trabalhando com arquivos de mídia digital que você forneceu. Nesse cenário, você sabe que os atributos específicos estão no arquivo. Ao adicionar o item de mídia à biblioteca, você sabe que pode trabalhar com esses atributos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> </dl>

 

 




