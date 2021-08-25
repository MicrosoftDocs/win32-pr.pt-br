---
description: o Windows o componente de geração de imagens (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows Visão geral do componente de geração de imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f4276a70b94fd190b7254d8d3d2666581c0c9dbb991dee3ac6e0568b6ee649
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772506"
---
# <a name="windows-imaging-component-overview"></a>Windows Visão geral do componente de geração de imagens

o Windows o componente de geração de imagens (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem. O WIC possibilita que ISVs (fornecedores independentes de software) e IHVs (fornecedores independentes de hardware) desenvolvam seus próprios codecs de imagem e obtenham o mesmo suporte de plataforma como formatos de imagem padrão (por exemplo, TIFF, JPEG, PNG, GIF, BMP e HDPhoto). Um único conjunto consistente de interfaces é usado para todo o processamento de imagem, independentemente do formato da imagem, de modo que qualquer aplicativo que use o WIC Obtenha suporte automático para novos formatos de imagem assim que o codec for instalado. A estrutura de metadados extensíveis possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.

Este tópico inclui as seções a seguir.

-   [Windows Recursos do componente de geração de imagens](#windows-imaging-component-features)
-   [Codecs nativos](#native-codecs)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Recursos do componente de geração de imagens

Os principais recursos do WIC são:

-   Permite que os desenvolvedores de aplicativos executem operações de processamento de imagens em qualquer formato de imagem por meio de um único conjunto consistente de interfaces comuns, sem a necessidade de conhecimento prévio de formatos de imagem específicos.
-   Fornece uma arquitetura "plug and Play" extensível para codecs de imagem, formatos de pixel e metadados, com a descoberta automática de tempo de execução de novos formatos.
-   Dá suporte à leitura e gravação de metadados arbitrários em arquivos de imagem, com a capacidade de preservar metadados não reconhecidos durante a edição.
-   Preserva dados de imagem de alta profundidade de bits, até 32 bits por canal, em todo o pipeline de processamento de imagens.
-   Fornece suporte interno para os formatos de imagem mais populares, formatos de pixel e esquemas de metadados.

## <a name="native-codecs"></a>Codecs nativos

O WIC inclui vários codecs internos. Os codecs padrão a seguir são fornecidos com a plataforma. 

| Codec                                                                                             | Tipos de MIME                       | Decodificadores | Codificadores |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| bmp (formato de Bitmap Windows), especificação bmp v5.                                                | image/bmp                        | Sim      | Sim      |
| GIF (Graphics Interchange Format 89A), especificação GIF 89A/89m                                  | image/gif                        | Sim      | Sim      |
| ICO (formato de ícone)                                                                                 | imagem/ico                        | Sim      | Não       |
| JPEG (Joint multigraphic Experts Group), JFIF Specification 1, 2                                  | imagem/JPEG, imagem/JPE, imagem/jpg | Sim      | Sim      |
| PNG (Portable Network Graphics), especificação de PNG 1,2                                            | image/png                        | Sim      | Sim      |
| TIFF (formato de arquivo de imagem marcada), especificação TIFF 6,0                                           | imagem/TIFF, imagem/TIF            | Sim      | Sim      |
| Windows Foto de mídia, [especificação de foto de HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | Image/vnd. ms-phot                | Sim      | Sim      |
| DDS (superfície do DirectDraw)                                                                          | Image/vnd. ms-DDS                 | Sim      | Sim      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[CODEC de exemplo AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
