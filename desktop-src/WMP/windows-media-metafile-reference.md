---
title: Windows Referência de metadados de mídia
description: Windows Referência de metadados de mídia
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Metadados de mídia, referência
- metafiles,reference
- referência para metadados Windows Mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b00cd604ec94c42ef90f08a8875edb4fda92ba8267c7e4a7d7b5505c2fb57932
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862256"
---
# <a name="windows-media-metafile-reference"></a>Windows Referência de metadados de mídia

Essa referência documenta elementos e extensões de nome de arquivo para Windows metadados de mídia. A referência é dividida nas seções a seguir.



| Seção                                                                                    | Descrição                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Windows Referência de elementos de metadados de mídia](windows-media-metafile-elements-reference.md) | Documenta elementos de metadados, incluindo definições, atributos e seus valores e condições especiais relacionadas a cada elemento. |
| [Extensões de nome de arquivo](file-name-extensions.md)                                           | Documenta extensões de nome de arquivo de metadados com regras e diretrizes sobre seu uso.                                                  |



 

Windows Os metadados de mídia são arquivos de texto que fornecem informações sobre um fluxo de arquivos e sua apresentação. Os metadados são baseados na sintaxe linguagem XML (XML) e são feitos de vários elementos do tipo XML com suas marcas e atributos. Cada elemento define uma configuração ou ação para mídia de streaming.

Há dois conjuntos de marcas de elemento disponíveis para metadados. Os metadados do lado do cliente têm um conjunto de elementos e os metadados do lado do servidor têm outro conjunto de elementos.

Se uma marca de elemento não tiver elementos filho (aqueles que modificam ou estão contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura no lugar de uma marca de fechamento. Se os elementos filho não aparecerem entre a marca de abertura e fechamento de um elemento, eles não serão elementos filho desse elemento e serão ignorados ou causarão um erro na sintaxe do metadado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre Windows metadados de mídia**](about-windows-media-metafiles.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Metadados de mídia**](windows-media-metafiles.md)
</dt> </dl>

 

 




