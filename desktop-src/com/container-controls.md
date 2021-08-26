---
title: Controles de contêiner
description: Controles de contêiner
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896436"
---
# <a name="container-controls"></a>Controles de contêiner

Conforme descrito acima, os controles de contêiner ActiveX controles que contêm visualmente outros controles. A ActiveX de controles especifica a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar controles de contêiner. Os contêineres também podem dar suporte a controles de contêiner sem dar suporte **a ISimpleFrameSite,** embora o comportamento não possa ser garantido. Por esse motivo, existe uma categoria de componente para controles SimpleFrameSite em que a funcionalidade completa dessa interface é necessária.

Para dar suporte a controles de contêiner sem implementar [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), um ActiveX contêiner de controle deve:

-   Ative todos os controles o tempo todo.
-   Repare os controles contidos no hWnd do controle que o contém.
-   Permaneça o pai do controle de contêiner.

 

 




