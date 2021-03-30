---
title: Usando o aplicativo de desktop de exemplo
description: Usando o aplicativo de desktop de exemplo
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635317"
---
# <a name="using-the-sample-desktop-application"></a>Usando o aplicativo de desktop de exemplo

O aplicativo de desktop de exemplo é uma janela básica de dois painéis, um pouco semelhante ao Windows Explorer. Ele permite que você procure o conteúdo de um dispositivo, usando uma exibição de árvore exibição de pastas no painel esquerdo e arquivos no painel direito. A raiz de cada árvore de pastas é logicamente considerada um dispositivo diferente, embora alguns dispositivos possam se representar como vários objetos (um para cada armazenamento raiz). Para ler as propriedades básicas de uma pasta ou de um arquivo, clique com o botão direito do mouse no objeto e selecione **Propriedades**.

Você pode excluir arquivos no dispositivo selecionando um arquivo no painel direito e selecionando **excluir** no menu **arquivo** . Para adicionar arquivos de mídia ao dispositivo, você pode arrastar arquivos da área de trabalho para o painel direito do programa. Observe que os arquivos devem ter um formato de mídia com suporte no dispositivo; arquivos de formatos inaceitáveis (arquivos que não são de mídia, como arquivos. txt ou formatos de mídia não suportados pelo dispositivo) não serão enviados para o dispositivo. (Observe que essa restrição é a do programa; O Windows Media Gerenciador de Dispositivos permite que você envie qualquer arquivo para um dispositivo se o dispositivo o aceitar.)

Para capturar eventos de retorno de chamada enviados para a interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , você deve marcar a opção "usar a interface de operação" no menu **Opções** .

O menu **Opções** também permite que você escolha se deseja usar várias interfaces mais avançadas com recursos compatíveis com dispositivos avançados.

O menu **contêineres** tem opções para permitir que você crie uma lista de reprodução ou um álbum. Para criar uma lista de reprodução, selecione uma ou mais músicas no dispositivo e clique em **criar playlist** no menu **contêineres** . Esse recurso funciona apenas em dispositivos MTP, pois o código só dá suporte à criação de um arquivo de playlist "virtual". (Uma playlist virtual é uma lista de reprodução que é especificada somente por valores de metadados, em vez de por um arquivo físico, por exemplo, um arquivo WPL.) O dispositivo deve dar suporte a listas de reprodução vazias para usar esse recurso.

Para criar um álbum (uma lista de reprodução com uma imagem associada), selecione uma ou mais músicas no dispositivo e clique em **criar álbum** no menu **contêineres** . Uma caixa de diálogo permite que você navegue até um arquivo de imagem no computador para associá-lo ao álbum. Da mesma forma que cria listas de reprodução, o aplicativo cria um arquivo de álbum "vazio"; Se o dispositivo não oferecer suporte a álbuns vazios, esse recurso não funcionará.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Aplicativo de desktop de exemplo**](sample-desktop-application.md)
</dt> </dl>

 

 




