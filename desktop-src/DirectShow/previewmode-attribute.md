---
description: O atributo PreviewMode especifica o modo de visualização para o grupo. Se o valor for TRUE, os quadros poderão ser removidos durante a visualização. Caso contrário, nenhum quadro será removido durante a visualização. O valor padrão é TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Atributo PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baed13417539432a3a2958b96b214c3c63ae12f2802586ca220669b1497d91f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748266"
---
# <a name="previewmode-attribute"></a>Atributo PreviewMode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `previewmode` atributo especifica o modo de visualização para o grupo. Se o valor for **true**, os quadros poderão ser removidos durante a visualização. Caso contrário, nenhum quadro será removido durante a visualização. O valor padrão é **true**.

## <a name="possible-values"></a>Valores possíveis

Os valores a seguir são definidos como TRUE: y, Y, t, T, 1. Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Aplica-se A

[**group**](group-element.md)

## <a name="remarks"></a>Comentários

Na configuração padrão, os quadros são descartados durante a visualização de efeitos ou transições lentas, para manter o vídeo sincronizado com o áudio. O vídeo pode parecer instável como resultado. Definir esse atributo como **false** força cada quadro a ser renderizado durante a visualização, possivelmente resultando no vídeo ficando fora de sincronia com o áudio. Os quadros nunca são descartados durante a gravação em um arquivo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup:: SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



