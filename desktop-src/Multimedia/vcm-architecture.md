---
title: Arquitetura do VCM
description: Arquitetura do VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- vídeo para Windows (VFW), arquitetura VCM
- VFW (vídeo para Windows), arquitetura VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7676fe7786b8674ddca957a75c33336294b65a9df18d53fe4b9c7f493092b66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135594"
---
# <a name="vcm-architecture"></a>Arquitetura do VCM

VCM é um intermediário entre um aplicativo e a compactação e os drivers de descompactação. Os drivers de compactação e descompactação compactam e descompactam quadros de dados individuais.

Quando um aplicativo faz uma chamada para VCM, o VCM converte a chamada em uma mensagem. A mensagem é enviada usando a função [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para o compactador ou o descompactador apropriado, que compacta ou descompacta os dados. O VCM recebe o valor de retorno do driver de compactação ou descompactação e, em seguida, retorna o controle para o aplicativo.

Se uma macro for definida para uma mensagem, a macro se expandirá para uma chamada de função **ICSendMessage** fornecendo os parâmetros apropriados para essa mensagem. Se uma macro for definida para uma mensagem, seu aplicativo deverá usá-la em vez da mensagem. Nesta visão geral, essas macros seguem mensagens entre parênteses.

 

 




