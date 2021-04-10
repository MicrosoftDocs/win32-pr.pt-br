---
description: O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Visão geral do Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169884"
---
# <a name="windows-imaging-component-overview"></a>Visão geral do Windows Imaging Component

O Windows Imaging Component (WIC) fornece uma estrutura extensível para trabalhar com imagens e metadados de imagem. O WIC possibilita que ISVs (fornecedores independentes de software) e IHVs (fornecedores independentes de hardware) desenvolvam seus próprios codecs de imagem e obtenham o mesmo suporte de plataforma como formatos de imagem padrão (por exemplo, TIFF, JPEG, PNG, GIF, BMP e HDPhoto). Um único conjunto consistente de interfaces é usado para todo o processamento de imagem, independentemente do formato da imagem, de modo que qualquer aplicativo que use o WIC Obtenha suporte automático para novos formatos de imagem assim que o codec for instalado. A estrutura de metadados extensíveis possibilita que os aplicativos leiam e gravem seus próprios metadados proprietários diretamente nos arquivos de imagem, para que os metadados nunca sejam perdidos ou separados da imagem.

Este tópico inclui as seções a seguir.

-   [Recursos do Windows Imaging Component](#windows-imaging-component-features)
-   [Codecs nativos](#native-codecs)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-imaging-component-features"></a>Recursos do Windows Imaging Component

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
| BMP (formato de bitmap do Windows), especificação BMP v5.                                                | image/bmp                        | Sim      | Sim      |
| GIF (Graphics Interchange Format 89A), especificação GIF 89A/89m                                  | image/gif                        | Sim      | Sim      |
| ICO (formato de ícone)                                                                                 | imagem/ico                        | Sim      | Não       |
| JPEG (Joint multigraphic Experts Group), JFIF Specification 1, 2                                  | imagem/JPEG, imagem/JPE, imagem/jpg | Sim      | Sim      |
| PNG (Portable Network Graphics), especificação de PNG 1,2                                            | image/png                        | Sim      | Sim      |
| TIFF (formato de arquivo de imagem marcada), especificação TIFF 6,0                                           | imagem/TIFF, imagem/TIF            | Sim      | Sim      |
| Foto do Windows Media, [especificação de foto de HD 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | Image/vnd. ms-phot                | Sim      | Sim      |
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

 

 
