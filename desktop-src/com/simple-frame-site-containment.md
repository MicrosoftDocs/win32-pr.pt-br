---
title: Contenção de site de quadro simples
description: Contenção de site de quadro simples
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d356d6cc4993702ac571a800ad2abbfe378e8a8fe06ddc80225d81f0fe21a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129848"
---
# <a name="simple-frame-site-containment"></a>Contenção de site de quadro simples

Um controle de contêiner é ActiveX controle que é capaz de conter outros controles. Uma caixa de grupo que contém uma coleção de botões de opção é um exemplo de um controle de contêiner. Os controles de contêiner devem definir o bit de status OLEMISC SIMPLEFRAME e devem chamar a implementação \_ [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) do contêiner. Um contêiner ActiveX controle que dá suporte a controles de contêiner deve implementar **ISimpleFrameSite**.

CATID – {157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




