---
title: Controles sem janelas
description: Controles sem janelas
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf529349a1e1987870b3aac01a69aef3dacbd700d0060cd2177c05479409c7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991986"
---
# <a name="windowless-controls"></a>Controles sem janelas

A especificação ActiveX Controls 96 inclui uma definição para controles sem janela. Esses controles não operam em sua própria janela e exigem um contêiner para oferecer uma janela compartilhada na qual o controle pode desenhar, consulte o SDK ActiveX. Os controles sem janela são projetados para serem compatíveis com contêineres de controle mais antigos criando sua própria janela nessa situação, os contêineres de controle sem janela devem hospedar controles em janelas da maneira tradicional, sem problemas. No entanto, pode ser útil para um contêiner distinguir esses controles que podem operar em um modo sem janela, portanto, uma categoria de componente apropriada é definida.

CATID – {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID \_ WindowlessObject

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




