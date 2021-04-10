---
title: Adicionando o atributo ContentDistributor
description: Adicionando o atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Lojas online do Windows Media Player, adicionando atributo ContentDistributor
- lojas online, adicionando o atributo ContentDistributor
- Digite 1 lojas online, adicionando o atributo ContentDistributor
- tipo 2 lojas online, adicionando atributo ContentDistributor
- Armazenamentos online do Windows Media Player, atributo ContentDistributor
- lojas online, atributo ContentDistributor
- Digite 1 lojas online, atributo ContentDistributor
- tipo 2 lojas online, atributo ContentDistributor
- adicionando atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292214"
---
# <a name="adding-the-contentdistributor-attribute"></a>Adicionando o atributo ContentDistributor

Quando o usuário tenta reproduzir o conteúdo da loja online ou copiar o conteúdo para um CD ou dispositivo, o Windows Media Player chama determinados métodos em seu objeto COM. Para fazer isso, o player precisa de uma maneira de diferenciar o conteúdo dos outros provedores de loja online. Ao adicionar o nome da sua chave de loja online como o valor para o **ContentDistributor** (que é um alias para o atributo do SDK do Windows Media Format chamado **WM/ContentDistributor**) ao conteúdo baseado no Windows Media, você garante que o Player possa identificar o conteúdo associado ao seu serviço.

A adição de um valor a **ContentDistributor** também garante que o Windows Media Player criará um nó na biblioteca para o conteúdo que você fornecer. Consulte [integração de biblioteca](library-integration.md).

Você pode especificar esse valor de duas maneiras:

-   Use o modelo de objeto do Windows Media Player. Quando você faz isso, o Windows Media Player adiciona o valor que você especifica ao banco de dados de biblioteca. Eventualmente, o Player também gravará o valor do atributo no arquivo de mídia digital.
-   Use o Windows Media Format SDK para adicionar programaticamente o atributo **WM/ContentDistributor** . Quando você faz isso, o Windows Media Player lê o valor do atributo e o adiciona ao banco de dados quando o arquivo de mídia digital é adicionado à biblioteca.

Ao criar seu objeto COM da loja online, o valor do atributo de arquivo definido para **ContentDistributor** e o valor atribuído à constante KszContentDistributorID em seuprojeto. h devem corresponder exatamente. Lembre-se de que você especificou esse valor constante para o objeto COM quando criou o projeto usando o assistente de projeto. Você pode alterar esse valor manualmente. Certifique-se de usar uma cadeia de caracteres que identifique exclusivamente seu serviço.

## <a name="using-the-windows-media-player-object-model"></a>Usando o modelo de objeto do Windows Media Player

Para especificar um valor para **ContentDistributor** usando o modelo de objeto do Windows Media Player, use o método [Media. setItemInfo](media-setiteminfo.md) . O código de exemplo a seguir especifica o valor "Proseware" para **ContentDistributor** para o item de mídia em execução no momento:


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>Usando o Windows Media Format SDK

O SDK do Windows Media Player inclui um arquivo C++ de exemplo, chamado SetContentDistributor. cpp, que demonstra como usar o SDK do Windows Media Format 9 Series para adicionar o atributo **WM/ContentDistributor** . Você pode localizar esse arquivo de exemplo na pasta denominada metadados onde você instalou o SDK. Para usar esse código, você deve seguir estas etapas:

1.  Instale o SDK da série 9 do Windows Media Format e configure o tempo de execução conforme descrito na documentação.
2.  Crie um novo projeto C++ vazio no Visual Studio e adicione o arquivo de exemplo chamado SetContentDistributor. cpp ao projeto.
3.  Adicione o caminho para as pastas de biblioteca do SDK do Windows Media Format 9 Series à lista de caminhos de arquivo. No menu **Ferramentas**, escolha **Opções**.
4.  Na caixa de diálogo **Opções** , clique em **projetos** e, em seguida, clique em **diretórios do vc + +**.
5.  Na caixa de listagem suspensa **Mostrar diretórios para** , clique em **arquivos de biblioteca**.
6.  Use os botões para adicionar os caminhos às caixas de listagem.
7.  Abra a caixa de diálogo páginas de propriedades do seu projeto. Escolha **Propriedades de configuração**, **vinculador** e, em seguida, **entrada**. Digite "WMVCORE. lib" na caixa de texto **dependências adicionais** .

O código de exemplo cria um programa de linha de comando. Os argumentos que você fornece ao executar o programa especificam o caminho para o arquivo de mídia digital a ser modificado e uma cadeia de caracteres para o valor do atributo **ContentDistributor** . O código usa **IWMHeaderInfo:: setAttribute** para adicionar o atributo ao arquivo especificado. Você pode usar este exemplo como está ou usá-lo como um ponto de partida para seu próprio programa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




