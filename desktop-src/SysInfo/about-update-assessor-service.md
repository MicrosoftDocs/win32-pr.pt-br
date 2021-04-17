---
description: O tópico a seguir descreve como a API da plataforma de avaliação WaaS (Windows as a Service) funciona.
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Sobre a plataforma de avaliação do WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756129"
---
# <a name="about-the-waas-assessment-platform"></a>Sobre a plataforma de avaliação do WaaS

O tópico a seguir descreve como a API da plataforma de avaliação WaaS (Windows as a Service) funciona.

A API de avaliação do WaaS oferece ao chamador as seguintes informações:

-   Se um dispositivo estiver nas atualizações mais recentes da Microsoft.
-   Se o dispositivo atingiu o fim do suporte.
-   Os tempos de liberação para as atualizações mais recentes aplicáveis para o dispositivo.
-   Uma avaliação do motivo pelo qual um dispositivo não está atualizado e o impacto potencial que ele pode ter no dispositivo.

A plataforma de avaliação do WaaS usa o modelo de API COM e é executada automaticamente pelo menos uma vez por dia. Esse ciclo captura as informações de versão aplicáveis. Durante o período em cache, as avaliações são feitas em relação às informações de versão armazenadas em cache. Se uma chamada for feita fora da janela de expiração do cache, uma nova chamada e uma avaliação serão feitas, armazenadas em cache e retornadas. Quando uma chamada é feita, o cliente de avaliação do WaaS entra em contato com o serviço de avaliação do WaaS com os atributos do dispositivo e recebe um dossiê de informações aplicáveis ao dispositivo. Em seguida, o cliente usa essas informações em relação às informações coletadas sobre o dispositivo para realizar a avaliação.

> [!NOTE]
> Seu código deve ter privilégios de administrador para chamar a API de avaliação do WAAS. Para obter mais detalhes sobre como desenvolver aplicativos que exigem privilégios de administrador, consulte [Este artigo](../secauthz/developing-applications-that-require-administrator-privilege.md).

 
