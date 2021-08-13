---
title: Adicionando o atributo ContentDistributor
description: Adicionando o atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player lojas online, adicionando o atributo ContentDistributor
- lojas online, adicionando o atributo ContentDistributor
- Digite 1 lojas online, adicionando o atributo ContentDistributor
- tipo 2 lojas online, adicionando atributo ContentDistributor
- Windows Media Player lojas online, atributo ContentDistributor
- lojas online, atributo ContentDistributor
- Digite 1 lojas online, atributo ContentDistributor
- tipo 2 lojas online, atributo ContentDistributor
- adicionando atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66871f73c03e73c08b5ae7e72518a48817192def22c8dfce4caf2ce12d36fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391786"
---
# <a name="adding-the-contentdistributor-attribute"></a>Adicionando o atributo ContentDistributor

quando o usuário tenta reproduzir o conteúdo da loja online ou copiar o conteúdo para um CD ou dispositivo, Windows Media Player chama determinados métodos em seu objeto COM. Para fazer isso, o player precisa de uma maneira de diferenciar o conteúdo dos outros provedores de loja online. adicionando o nome da sua chave de loja online como o valor para **ContentDistributor** (que é um alias para o atributo Windows media Format SDK denominado **WM/ContentDistributor**) para o conteúdo baseado em mídia do Windows, você garante que o Player possa identificar o conteúdo associado ao seu serviço.

a adição de um valor a **ContentDistributor** também garante que Windows Media Player criará um nó na biblioteca para o conteúdo que você fornecer. Consulte [integração de biblioteca](library-integration.md).

Você pode especificar esse valor de duas maneiras:

-   Use o modelo de objeto Windows Media Player. quando você fizer isso, Windows Media Player adicionará o valor que você especificar ao banco de dados de biblioteca. Eventualmente, o Player também gravará o valor do atributo no arquivo de mídia digital.
-   Use o SDK do formato de mídia Windows para adicionar programaticamente o atributo **WM/ContentDistributor** . ao fazer isso, Windows Media Player lê o valor do atributo e o adiciona ao banco de dados quando o arquivo de mídia digital é adicionado à biblioteca.

Ao criar seu objeto COM da loja online, o valor do atributo de arquivo definido para **ContentDistributor** e o valor atribuído à constante KszContentDistributorID em seuprojeto. h devem corresponder exatamente. Lembre-se de que você especificou esse valor constante para o objeto COM quando criou o projeto usando o assistente de projeto. Você pode alterar esse valor manualmente. Certifique-se de usar uma cadeia de caracteres que identifique exclusivamente seu serviço.

## <a name="using-the-windows-media-player-object-model"></a>usando o modelo de objeto Windows Media Player

para especificar um valor para **ContentDistributor** usando o modelo de objeto Windows Media Player, use o método [Media. setItemInfo](media-setiteminfo.md) . O código de exemplo a seguir especifica o valor "Proseware" para **ContentDistributor** para o item de mídia em execução no momento:


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



## <a name="using-the-windows-media-format-sdk"></a>usando o SDK do formato de mídia Windows

o sdk do Windows Media Player inclui um arquivo C++ de exemplo, chamado SetContentDistributor. cpp, que demonstra como usar o SDK do Windows Media Format 9 Series para adicionar o atributo **WM/ContentDistributor** . Você pode localizar esse arquivo de exemplo na pasta denominada metadados onde você instalou o SDK. Para usar esse código, você deve seguir estas etapas:

1.  instale o SDK da série 9 do formato de mídia do Windows e configure o tempo de execução conforme descrito na documentação.
2.  crie um novo projeto C++ vazio no Visual Studio e adicione o arquivo de exemplo chamado SetContentDistributor. cpp ao projeto.
3.  adicione o caminho às pastas de biblioteca do SDK do Windows Media Format 9 Series à lista de caminhos de arquivo. No menu **Ferramentas**, escolha **Opções**.
4.  na caixa de diálogo **opções** , clique em **projetos** e, em seguida, clique em **diretórios VC++**.
5.  Na caixa de listagem suspensa **Mostrar diretórios para** , clique em **arquivos de biblioteca**.
6.  Use os botões para adicionar os caminhos às caixas de listagem.
7.  Abra a caixa de diálogo páginas de propriedades do seu projeto. Escolha **Propriedades de configuração**, **vinculador** e, em seguida, **entrada**. Digite "WMVCORE. lib" na caixa de texto **dependências adicionais** .

O código de exemplo cria um programa de linha de comando. Os argumentos que você fornece ao executar o programa especificam o caminho para o arquivo de mídia digital a ser modificado e uma cadeia de caracteres para o valor do atributo **ContentDistributor** . O código usa **IWMHeaderInfo:: setAttribute** para adicionar o atributo ao arquivo especificado. Você pode usar este exemplo como está ou usá-lo como um ponto de partida para seu próprio programa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




