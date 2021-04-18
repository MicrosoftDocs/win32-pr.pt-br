---
description: Há algumas considerações que são exclusivas para sistemas administrados remotamente.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerações sobre administração remota de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784506"
---
# <a name="wfp-remote-administration-considerations"></a>Considerações sobre administração remota de WFP

Há algumas considerações que são exclusivas para sistemas administrados remotamente. Primeiro, quando a instalação de software é implantada remotamente (usando SMS ou MSI), as caixas de diálogo de erro WFP são exibidas na tela de um administrador conectado localmente (se houver), não no serviço de instalação. Em segundo lugar, se um administrador fizer logon em um servidor de terminal remotamente e instalar um aplicativo que substitui arquivos do sistema protegidos, as caixas de diálogo de erro WFP serão exibidas somente no console principal, não na janela remota do administrador.

Por esses motivos, a WFP suprime suas caixas de diálogo de erro até que um administrador faça logon localmente. Os administradores remotos podem encontrar erros de substituição de arquivo no log de eventos do sistema.

**Windows Vista e Windows Server 2008:** Não há suporte para a administração remota de WFP.

 

 



