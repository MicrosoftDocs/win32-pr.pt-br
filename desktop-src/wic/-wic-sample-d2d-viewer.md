---
description: Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar um arquivo de imagem e Direct2D para renderizar a imagem na tela.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visualizador de imagem de WIC usando o exemplo de Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105751160"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>Visualizador de imagem de WIC usando o exemplo de Direct2D

Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar um arquivo de imagem e Direct2D para renderizar a imagem na tela.

## <a name="requirements"></a>Requisitos

Este exemplo tem os seguintes requisitos.

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows Vista |
| SDK do Windows mínimo | [SDK (Software Development Kit)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) do Windows para Windows 7 |

## <a name="downloading-the-sample"></a>Baixar o exemplo

Este exemplo está disponível no [Visualizador do WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).

## <a name="building-the-sample"></a>Compilando o exemplo

### <a name="using-visual-studio-preferred-method"></a>Usando o Visual Studio (método preferencial)

1. Abra o Windows Explorer e navegue para o diretório.
2. Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo no Visual Studio.
3. No menu **Compilar**, selecione **Compilar Solução**. O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.

### <a name="using-the-command-prompt"></a>Usando o prompt de comando

Para criar o exemplo usando um prompt de comando:

1. Abra uma janela de prompt de comando e navegue até o diretório de exemplo.
2. Digite `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>Executando o exemplo

Depois de iniciar o aplicativo, carregue um arquivo de imagem usando o comando **abrir** do menu **arquivo** .

## <a name="see-also"></a>Confira também

[Codec de imagem do Microsoft Windows](-wic-lh.md)

[Guia de programação](-wic-programming-guide.md)

[Referência](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Amostras e exemplos de código](-wic-samples.md)
