---
description: este exemplo demonstra o uso do Windows o componente de geração de imagens (WIC) para decodificar uma imagem que é codificada com níveis progressivos.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Exemplo de decodificação progressiva de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 26e26670aad4e3aeed8fca167d77ba6ad36b931d738fccf9717c6e119bf943a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032023"
---
# <a name="wic-progressive-decoding-sample"></a>Exemplo de decodificação progressiva de WIC

este exemplo demonstra o uso do Windows o componente de geração de imagens (WIC) para decodificar uma imagem que é codificada com níveis progressivos. este exemplo usa Direct2D para renderizar os diferentes níveis progressivos na tela.

## <a name="requirements"></a>Requisitos

Este exemplo tem os seguintes requisitos.

| Requisito | Valor |
|-|
| Cliente mínimo com suporte | Windows 7 |
| SDK do Windows mínimo | [SDK (Software Development Kit) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para Windows 7 |

## <a name="downloading-the-sample"></a>Baixar o exemplo

Este exemplo está disponível na [codificação progressiva do WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).

## <a name="building-the-sample"></a>Compilando o exemplo

### <a name="using-visual-studio-preferred-method"></a>usando Visual Studio (método preferencial)

1. Abra o Windows Explorer e navegue para o diretório.
2. Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo em Visual Studio.
3. No menu Compilar, selecione Compilar Solução. O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.

### <a name="using-the-command-prompt"></a>Usando o prompt de comando

Para criar o exemplo usando o prompt de comando.

1. Abra o prompt de comando e navegue até o diretório de exemplo.
2. Digite `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Executando o exemplo

Depois que o aplicativo for iniciado, carregue um arquivo de imagem por meio do menu abrir arquivo. Ao carregar, o nível progressivo padrão é definido como 0. Você pode navegar para diferentes níveis progressivos por meio de menu ou de uma tecla para cima/para baixo. O texto do nível progressivo atual é exibido na barra de status da janela principal. Há suporte para o redimensionamento de janela.

> [!NOTE]
> A decodificação progressiva está disponível apenas para imagens que foram codificadas progressivamente. A imagem fornecida com este exemplo foi codificada progressivamente.

## <a name="see-also"></a>Confira também

[Codec do Microsoft Windows Imaging](-wic-lh.md)

[Guia de programação](-wic-programming-guide.md)

[Referência](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Amostras e exemplos de código](-wic-samples.md)

[Visão geral da decodificação progressiva](-wic-progressive-decoding.md)
