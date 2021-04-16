---
description: Demonstra como adicionar itens à lista de atalhos automática para um aplicativo, incluindo a alternância entre a exibição das categorias frequentes e recentes.
title: Exemplo de lista de atalhos automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461270"
---
# <a name="automatic-jump-list-sample"></a>Exemplo de lista de atalhos automática

Demonstra como adicionar itens à lista de atalhos automática para um aplicativo, incluindo a alternância entre a exibição das categorias frequentes e recentes.

Este tópico inclui as seções a seguir.

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de AutomaticJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **AutomaticJumpList** .
2.  Digite `msbuild AutomaticJumpListSample.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **AutomaticJumpList** .
2.  Clique duas vezes no ícone do arquivo AutomaticJumpListSample. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `AutomaticJumpListSample.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para AutomaticJumpListSample.exe.
3.  Este exemplo deve ser executado como administrador na primeira vez em que for executado para que ele possa instalar os registros de tipo de arquivo necessários. Depois que os tipos de arquivo tiverem sido registrados, o exemplo poderá ser executado como um usuário padrão.
4.  Selecione opções no menu do aplicativo de exemplo, incluindo a seleção de documentos. txt ou. doc por meio da caixa de diálogo **abrir** para ver como eles afetam a lista de atalhos do aplicativo na barra de tarefas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



