---
title: Controles de contêiner
description: Controles de contêiner
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69228bcc03017442880d41156f67397ee26bb13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453732"
---
# <a name="container-controls"></a>Controles de contêiner

Conforme descrito acima, os controles de contêiner são controles ActiveX que contêm visualmente outros controles. A arquitetura de controles ActiveX especifica a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para habilitar controles de contêiner. Os contêineres também podem dar suporte a controles de contêiner sem dar suporte a **ISimpleFrameSite**, embora o comportamento não possa ser garantido. Por esse motivo, existe uma categoria de componente para controles SimpleFrameSite em que a funcionalidade completa dessa interface é necessária.

Para dar suporte a controles de contêiner sem implementar [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), um contêiner de controle ActiveX deve:

-   Ative todos os controles em todos os momentos.
-   Reparente os controles contidos para o hWnd do controle que o contém.
-   Permanecerá o pai do controle de contêiner.

 

 




