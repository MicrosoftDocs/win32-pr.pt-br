---
description: Efeito Alfa Setter
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efeito Alfa Setter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e599b314dced175188d77dad1ae93259a23b8eb892471d047afab218add9a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586756"
---
# <a name="alpha-setter-effect"></a>Efeito Alfa Setter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O efeito Alfa Setter define os bits alfa em uma imagem de vídeo.

CLSID (ID de classe): {506D89AE-909A-44f7-9444-CELL575896E35}

Nome da variável CLSID: CLSID \_ DxtAlphaSetter

Nome amigável: "DxtAlphaSetter"

### <a name="properties"></a>Propriedades



| Propriedade  | Type   | Padrão | Descrição                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alpha     | BYTE   | -1      | Define o alfa para toda a imagem.                        |
| AlphaRamp | double | -1.0    | Define o alfa como uma porcentagem do valor alfa original. |



 

## <a name="remarks"></a>Comentários

Uma propriedade com um valor negativo é ignorada. Somente uma propriedade pode ter um valor não negativo. A propriedade Alfa especifica um valor alfa constante para cada pixel na imagem. Essa propriedade substitui os valores alfa da imagem original. A propriedade AlphaRamp especifica o valor alfa de cada pixel como uma porcentagem do valor original do pixel, de 0,0 a 1,0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Combinação alfa](alpha-blending.md)
</dt> </dl>

 

 



