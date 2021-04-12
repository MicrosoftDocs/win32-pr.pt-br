---
title: Controles sem janelas
description: Controles sem janelas
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364468"
---
# <a name="windowless-controls"></a>Controles sem janelas

A especificação de controles ActiveX 96 inclui uma definição para controles sem janela. Esses controles não operam em sua própria janela e exigem um contêiner para oferecer uma janela compartilhada na qual o controle pode desenhar, consulte o SDK do ActiveX. Os controles sem janela são projetados para serem compatíveis com contêineres de controle mais antigos criando sua própria janela nessa situação, os contêineres de controle sem janela devem hospedar controles de janela da maneira tradicional sem problemas. No entanto, pode ser útil para um contêiner distinguir os controles que podem operar em modo sem janela, portanto, uma categoria de componente apropriada é definida.

CATID-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




