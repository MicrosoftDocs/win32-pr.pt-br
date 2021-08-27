---
description: Há algumas considerações que são exclusivas para sistemas administrados remotamente.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerações sobre administração remota do WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b3106a02aa4098d2814a955e6582d6e8f1c79f7f161a6875891e13a0db71a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098586"
---
# <a name="wfp-remote-administration-considerations"></a>Considerações sobre administração remota do WFP

Há algumas considerações que são exclusivas para sistemas administrados remotamente. Primeiro, quando a instalação de software é implantada remotamente (usando SMS ou MSI), as caixas de diálogo de erro do WFP são exibidas na tela de um administrador conectado localmente (se presente), não no serviço de instalação. Em segundo lugar, se um administrador faz o login em um servidor de terminal remotamente e instala um aplicativo que substitui arquivos do sistema protegidos, as caixas de diálogo de erro do WFP são exibidas somente no console principal, não na janela remota do administrador.

Por esses motivos, o WFP suprime suas caixas de diálogo de erro até que um administrador entre localmente. Os administradores remotos podem encontrar erros de substituição de arquivo no log de eventos do sistema.

**Windows Vista e Windows Server 2008:** Não há suporte para a administração remota do WFP.

 

 



