---
description: Demonstra como criar um verbo que opera em itens de shell e contêineres que reproduz itens ou adiciona itens a uma fila.
title: Exemplo de verbo do player
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169908"
---
# <a name="player-verb-sample"></a>Exemplo de verbo do player

Demonstra como criar um verbo que opera em itens de shell e contêineres que reproduz itens ou adiciona itens a uma fila. Este exemplo é particularmente útil para aplicativos de mídia.

Este tópico inclui as seções a seguir.

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de PlayerVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **PlayerVerbSample** .
2.  Digite `msbuild PlayerVerbSample.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **PlayerVerbSample** .
2.  Clique duas vezes no ícone do arquivo PlayerVerbSample. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `PlayerVerbSample.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para PlayerVerbSample.exe.
3.  Selecione `Register Verbs` na caixa de diálogo **exemplo de verbo do Player** .
4.  Clique com o botão direito do mouse em itens de imagem (arquivo, pasta ou pilha) no Windows Explorer para adicioná-los a uma fila ou reproduzi-los no aplicativo de exemplo. Use itens de música quando alterar o exemplo para trabalhar com música.

 

 



