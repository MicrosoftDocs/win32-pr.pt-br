---
title: Criando um pacote de download do Windows Media (preterido)
description: Criando um pacote de download do Windows Media (preterido)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, criando
- Criando pacotes de download do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005724"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Criando um pacote de download do Windows Media (preterido)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

Siga estas etapas para criar um pacote de download do Windows Media.

1.  **Criar uma borda.** Use as mesmas técnicas que você usaria para criar uma capa para o Windows Media Player. Projete a borda para que o redimensionamento do Windows Media Player não arruinar a composição dos elementos de borda. Por exemplo, use uma cor sólida ou uma visualização como um plano de fundo, pois elas serão dimensionadas corretamente à medida que o Windows Media Player for redimensionado.
2.  **Compactar o conteúdo da borda.** Crie uma pasta compactada (com uma extensão de nome de arquivo. zip) que contenha os arquivos de borda: imagens, arquivos JScript e o arquivo de definição de capa com uma extensão de nome de arquivo. WMS. Renomeie o arquivo compactado para que ele tenha uma extensão de nome de arquivo. wmz.
3.  **Escreva um metarquivo do Windows Media.** O Windows Media Player não carregará a borda, a menos que você crie um metarquivo do Windows Media com uma extensão de nome de arquivo. asx que implemente o elemento **Skin** . O metarquivo também pode ser usado para criar uma lista de reprodução que descreve o conteúdo incluído no pacote.
4.  **Monte seu conteúdo.** Coloque todos os arquivos que você deseja usar em uma pasta. Isso inclui arquivos de áudio, arquivos de vídeo, metaarquivos e arquivos de definição de borda.
5.  **Crie o pacote.** Crie uma pasta compactada (com uma extensão de nome de arquivo. zip) que contenha o arquivo de borda, arquivos de conteúdo e o metarquivo. Altere a extensão de nome de arquivo desse arquivo. zip para uma extensão de nome de arquivo. WMD.
6.  **Poste o pacote em um site.** O pacote concluído está pronto para ser Postado em um site e baixado pelos usuários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Pacotes de download do Windows Media (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




