---
title: Visual Basic interfaces privadas
description: Visual Basic interfaces privadas
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006164"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic interfaces privadas

Duas interfaces implementadas por Visual Basic são identificadas aqui para categorias de componentes. Não é esperado que os controles exijam essas categorias porque é possível que os controles ofereçam funcionalidade alternativa quando não estão disponíveis.

A interface [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que os controles se integrem melhor ao ambiente de Visual Basic ao formatar dados.

CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

A interface [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite que um controle enumere outros controles no formulário do VB.

CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Duas interfaces privadas adicionais, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), são descritas aqui, mesmo que não definam categorias de componentes. Não é recomendável usar essas quatro interfaces porque elas não têm suporte em contêineres diferentes de Visual Basic.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




