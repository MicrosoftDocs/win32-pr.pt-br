---
description: Demonstra como usar os métodos de interface IFileOperationProgressSink para monitorar os detalhes das ações da interface IFileOperation.
title: Coletor do andamento da operação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fe0ba5c86fdb2df5fe168559aa019941897563823e75670b0813ecb7e9e44d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820346"
---
# <a name="file-operation-progress-sink"></a>Coletor do andamento da operação de arquivo

Demonstra como usar os métodos de interface [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) para monitorar os detalhes das ações da interface [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .

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



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de FileOperationProgressSink](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo na janela de prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **FileOperationProgressSink** .
2.  Digite `msbuild FileOperationProgressSinkSample.sln`.

para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  abra Windows Explorer e navegue até o diretório do projeto **FilesInUse** . Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .
2.  Clique duas vezes no ícone do arquivo FileOperationProgressSinkSample. sln para abrir o projeto no Visual Studio.
    > [!Note]  
    > A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão. nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".

     

3.  No menu **Compilar**, selecione **Compilar Solução**.

## <a name="running-the-sample"></a>Executando o exemplo

1.  navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou Windows Explorer.
2.  no prompt de comando, digite `FileOperationProgressSinkSample.exe` ou, no Windows Explorer, clique duas vezes no ícone para FileOperationProgressSinkSample.exe.

 

 



