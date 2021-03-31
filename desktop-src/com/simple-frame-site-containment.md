---
title: Confinamento de site de quadro simples
description: Confinamento de site de quadro simples
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916125"
---
# <a name="simple-frame-site-containment"></a>Confinamento de site de quadro simples

Um controle de contêiner é um controle ActiveX capaz de conter outros controles. Uma caixa de grupo que contém uma coleção de botões de opção é um exemplo de um controle de contêiner. Os controles de contêiner devem definir o \_ bit de status OLEMISC SIMPLEFRAME e devem chamar a implementação de [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) do contêiner. Um contêiner de controle ActiveX que dá suporte a controles de contêiner deve implementar **ISimpleFrameSite**.

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

 




