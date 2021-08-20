---
description: Demonstra como personalizar a caixa de diálogo Arquivo em Uso para exibir informações e opções adicionais para arquivos que estão abertos no aplicativo no momento.
title: Exemplo do arquivo em uso
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27e0a216aed33d7b0295303539c6f46e489b4c4cba37fa7aedf0a7f2eddd7b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968795"
---
# <a name="file-is-in-use-sample"></a>Exemplo do arquivo em uso

Demonstra como personalizar a caixa de **diálogo Arquivo em** Uso para exibir informações e opções adicionais para arquivos que estão abertos no aplicativo no momento.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

Para obter requisitos adicionais, consulte o arquivosample.docx IFileIsInUse \_ incluído no exemplo.

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de FileIsInUse](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo na janela prompt de comando:

1.  Abra a janela Prompt de Comando e navegue **até o diretório do projeto FileIsInUse.**
2.  Digite `msbuild FileIsInUse.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra Windows Explorer e navegue até o **diretório do projeto FilesInUse.** Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .
2.  Clique duas vezes no ícone do arquivo FileIsInUseSample.sln para abrir o projeto Visual Studio.
    > [!Note]  
    > A extensão de nome de arquivo .sln não é mostrada nas configurações de pasta padrão. Nessa situação, ele pode ser identificado por seu ícone exclusivo ou por sua descrição de tipo, "Microsoft Visual Studio Solução".

     

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Navegue até o diretório que contém o novo executável, usando a janela do prompt de comando ou Windows Explorer.
2.  No prompt de comando, insira ou, Windows Explorer, clique duas vezes `FileIsInUseSample.exe` no ícone para FileIsInUseSample.exe.

Para obter informações detalhadas sobre este exemplo de código, consulte o arquivosample.docx IFileIsInUse \_ incluído no exemplo.

 

 



