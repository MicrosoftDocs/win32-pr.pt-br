---
title: Arquitetura do VCM
description: Arquitetura do VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Vídeo para Windows (VFW), arquitetura VCM
- VFW (vídeo para Windows), arquitetura de VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292453"
---
# <a name="vcm-architecture"></a>Arquitetura do VCM

VCM é um intermediário entre um aplicativo e a compactação e os drivers de descompactação. Os drivers de compactação e descompactação compactam e descompactam quadros de dados individuais.

Quando um aplicativo faz uma chamada para VCM, o VCM converte a chamada em uma mensagem. A mensagem é enviada usando a função [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) para o compactador ou o descompactador apropriado, que compacta ou descompacta os dados. O VCM recebe o valor de retorno do driver de compactação ou descompactação e, em seguida, retorna o controle para o aplicativo.

Se uma macro for definida para uma mensagem, a macro se expandirá para uma chamada de função **ICSendMessage** fornecendo os parâmetros apropriados para essa mensagem. Se uma macro for definida para uma mensagem, seu aplicativo deverá usá-la em vez da mensagem. Nesta visão geral, essas macros seguem mensagens entre parênteses.

 

 




