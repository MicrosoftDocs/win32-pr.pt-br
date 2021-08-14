---
description: criar seu codec na plataforma do Windows Imaging Component (WIC) possibilita que todos os aplicativos criados no wic obtenham o mesmo suporte de plataforma para o formato de imagem que eles obtêm para os formatos de imagem comuns fornecidos com a plataforma.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusão (como escrever um codec de WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5288438ea518e1776562b288184067df6d82c326eb6786b163f20e90c6febc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205817"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusão (como escrever um codec de WIC-Enabled)

criar seu codec na plataforma do Windows Imaging Component (WIC) possibilita que todos os aplicativos criados no wic obtenham o mesmo suporte de plataforma para o formato de imagem que eles obtêm para os formatos de imagem comuns fornecidos com a plataforma. ele também permite que a galeria de fotos Windows Vista, o Windows Explorer e o visualizador de fotos exibam miniaturas e visualizações de imagens em seu formato usando o decodificador que você fornecer. Para formatos brutos, ele permite que aplicativos mais sofisticados de geração de imagens aproveitem os recursos de processamento bruto do decodificador. Dependendo das opções de codificador que você dá suporte, você também pode expor recursos exclusivos do codificador para permitir que os aplicativos aproveitem ao máximo os recursos avançados do seu formato de imagem.

O desenvolvimento de um codec habilitado para WIC exige que você implemente algumas interfaces novas. Em muitos casos, você pode escrever um wrapper para o codec existente que implementa essas interfaces. Ao instalar o codec, você deve fazer algumas entradas do registro para tornar o codec detectável pela plataforma do WIC e associá-lo aos manipuladores de metadados apropriados. Você também precisa invocar uma API para limpar o cache de miniatura de qualquer miniatura padrão (vazia) que possa ter sido associada anteriormente às imagens no seu formato. se desejar, você poderá habilitar a galeria de fotos do Windows Vista para fornecer aos usuários um link para baixar seu codec quando a galeria de fotos encontrar uma imagem com a extensão de nome de arquivo. Para fazer isso, você deve fornecer à Microsoft informações sobre a extensão de nome de arquivo do codec e a URL para seu site de download.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Instalação e registro de CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de geração de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



