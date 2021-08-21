---
title: Visual Basic Interfaces privadas
description: Visual Basic Interfaces privadas
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd69e70d351245ebafa62d521a133726be568a0437f4e04ece4ef761535f4625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047704"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Interfaces privadas

Duas interfaces implementadas pelo Visual Basic são identificadas aqui para categorias de componentes. Não é esperado que os controles deverão exigir essas categorias, pois é possível que os controles ofereçam funcionalidade alternativa quando eles não estão disponíveis.

A [**interface IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que os controles se integrem melhor ao ambiente Visual Basic ao formatar dados.

CATID – {02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

A [**interface IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite que um controle enumere outros controles no formulário VB.

CATID – {02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Duas interfaces privadas adicionais, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject,**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)são descritas aqui mesmo que não definam categorias de componente. O uso dessas quatro interfaces não é recomendado porque não há suporte para contêineres que não Visual Basic.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




