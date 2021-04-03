---
description: Efeito de setter alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efeito de setter alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645867"
---
# <a name="alpha-setter-effect"></a>Efeito de setter alfa

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O efeito de setter alfa define os bits alfa em uma imagem de vídeo.

ID de classe (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}

Nome da variável CLSID: CLSID \_ DxtAlphaSetter

Nome amigável: "DxtAlphaSetter"

### <a name="properties"></a>Propriedades



| Propriedade  | Type   | Padrão | Descrição                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Define o alfa para a imagem inteira.                        |
| AlphaRamp | double | -1,0    | Define o alfa como um percentual do valor alfa original. |



 

## <a name="remarks"></a>Comentários

Uma propriedade com um valor negativo é ignorada. Apenas uma propriedade pode ter um valor não negativo. A propriedade Alpha especifica um valor alfa constante para cada pixel na imagem. Essa propriedade substitui os valores Alfa da imagem original. A propriedade AlphaRamp especifica o valor alfa de cada pixel como uma porcentagem do valor original do pixel, de 0,0 a 1,0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem alfa](alpha-blending.md)
</dt> </dl>

 

 



