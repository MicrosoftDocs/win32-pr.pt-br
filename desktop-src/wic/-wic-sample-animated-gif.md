---
description: Este exemplo demonstra a decodificação de vários quadros em um arquivo GIF, a leitura de metadados apropriados para cada quadro, a composição de quadros e a renderização da animação com Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Exemplo de GIF animado do WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 925beb45b58bdecb7d12505a9d2067cbcb9e6fbf1867786286f18333fea986e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709594"
---
# <a name="wic-animated-gif-sample"></a>Exemplo de GIF animado por WIC

Este exemplo demonstra a decodificação de vários quadros em um arquivo GIF, a leitura de metadados apropriados para cada quadro, a composição de quadros e a renderização da animação com Direct2D.

## <a name="requirements"></a>Requisitos

Este exemplo tem os seguintes requisitos.

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 7 |
| SDK do Windows mínimo | [SDK (Software Development Kit) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Baixar o exemplo

Este exemplo está disponível em [GIF animado por WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).

## <a name="building-the-sample"></a>Compilando o exemplo

### <a name="using-visual-studio-preferred-method"></a>usando Visual Studio (método preferencial)

1. Abra o Windows Explorer e navegue para o diretório.
2. Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo em Visual Studio.
3. No menu **Compilar**, selecione **Compilar Solução**. O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.

### <a name="using-the-command-prompt"></a>Usando o prompt de comando

Para criar o exemplo usando um prompt de comando.

1. Abra o prompt de comando e navegue até o diretório de exemplo.
2. Digite `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Executando o exemplo

Depois que o aplicativo for iniciado, carregue um arquivo de imagem usando o comando **abrir** do menu **arquivo** . Há suporte para o redimensionamento de janela.

## <a name="see-also"></a>Confira também

[Codec do Microsoft Windows Imaging](-wic-lh.md)

[Guia de programação](-wic-programming-guide.md)

[Referência](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Amostras e exemplos de código](-wic-samples.md)
