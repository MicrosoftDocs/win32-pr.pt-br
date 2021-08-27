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
ms.openlocfilehash: 4dcb2146c8db8eda0280b3ff7a34a19faf4ac172036ae7a4e61131b50fde2d0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090186"
---
# <a name="automatic-jump-list-sample"></a>Exemplo de lista de atalhos automática

Demonstra como adicionar itens à lista de atalhos automática para um aplicativo, incluindo a alternância entre a exibição das categorias frequentes e recentes.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
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

para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  abra Windows Explorer e navegue até o diretório do projeto **AutomaticJumpList** .
2.  Clique duas vezes no ícone do arquivo AutomaticJumpListSample. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  navegue até o diretório que contém o novo executável, usando o prompt de comando ou o gerenciador de Windows.
2.  Na linha de comando, digite `AutomaticJumpListSample.exe` . como alternativa, no Windows Explorer, clique duas vezes no ícone para AutomaticJumpListSample.exe.
3.  Este exemplo deve ser executado como administrador na primeira vez em que for executado para que ele possa instalar os registros de tipo de arquivo necessários. Depois que os tipos de arquivo tiverem sido registrados, o exemplo poderá ser executado como um usuário padrão.
4.  Selecione opções no menu do aplicativo de exemplo, incluindo a seleção de .txt ou .doc documentos por meio da caixa de diálogo **abrir** para ver como eles afetam a lista de atalhos do aplicativo na barra de tarefas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



