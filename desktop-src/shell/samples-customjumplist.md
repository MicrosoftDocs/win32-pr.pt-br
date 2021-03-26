---
description: Demonstra como criar uma lista de atalhos personalizada para um aplicativo, incluindo adicionar uma categoria e tarefas personalizadas.
title: Exemplo de lista de atalhos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170694"
---
# <a name="custom-jump-list-sample"></a>Exemplo de lista de atalhos personalizada

Demonstra como criar uma lista de atalhos personalizada para um aplicativo, incluindo adicionar uma categoria e tarefas personalizadas.

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
| GitHub  | [Exemplo de CustomJumpList](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **CustomJumpList** .
2.  Digite `msbuild CustomJumpListSample.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra o Windows Explorer e navegue até o diretório do projeto **CustomJumpList** .
2.  Clique duas vezes no ícone do arquivo CustomJumpListSample. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar** , selecione **Compilar solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.
2.  Na linha de comando, digite `CustomJumpListSample.exe` . Como alternativa, no Windows Explorer, clique duas vezes no ícone para CustomJumpListSample.exe.
3.  Este exemplo deve ser executado como administrador na primeira vez em que for executado para que ele possa instalar os registros de tipo de arquivo necessários. Depois que os tipos de arquivo tiverem sido registrados, o exemplo poderá ser executado como um usuário padrão.
4.  Selecione opções no menu do aplicativo de exemplo para ver como elas afetam a lista de atalhos do aplicativo na barra de tarefas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](appids.md)
</dt> </dl>

 

 



