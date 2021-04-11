---
description: Escolhendo um codec de áudio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Escolhendo um codec de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164217"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Escolhendo um codec de áudio (Microsoft Media Foundation)

O [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md) fornece três categorias de codificação de áudio, conforme mostrado na tabela a seguir.



| Categoria                         | Finalidade                                                    |
|----------------------------------|------------------------------------------------------------|
| Padrão de áudio do Windows Media     | Compactação de uso geral de áudio.                      |
| Windows Media Audio Professional | Compactação de áudio de alta definição e de vários canais.       |
| Windows Media Audio sem perdas     | Compactação de áudio sem perder nenhum dos dados originais. |



 

A categoria padrão fornece codificação de áudio de uso geral adequada para uma variedade de cenários de reprodução. Por exemplo, ele pode compactar áudio para uma taxa de bits baixa para streaming em uma rede com largura de banda limitada ou para renderização em dispositivos portáteis. Na outra extremidade da escala, ele pode produzir conteúdo de áudio compactado para reprodução de alta qualidade. A ênfase dos algoritmos de codificação padrão está em música, mas eles são adequados para outros conteúdos de áudio complexos também. A categoria padrão deve ser seu padrão de conteúdo de áudio. As categorias Professional e Lossless devem ser usadas para atender a necessidades específicas.

Um codificador separado, o [**codificador do Windows Media Voice**](windowsmediaaudiovoiceencoder.md), fornece a compactação de fala.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com áudio](workingwithaudio.md)
</dt> </dl>

 

 



