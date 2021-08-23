---
title: Níveis de proteção de saída
description: Níveis de proteção de saída
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- Windows SDK de Formato de Mídia, níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- níveis de proteção de saída (OPL)
- OPL (níveis de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76804b70df5db085484cb769e4c60f046aedadd9cd177480de90b8a3eb5ad6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707456"
---
# <a name="output-protection-levels"></a>Níveis de proteção de saída

As OPLs (níveis de proteção de saída) são classificações numéricas associadas a várias tecnologias que recebem conteúdo de mídia digital. O nível ao qual uma tecnologia dá suporte depende de quão segura ela é. O sistema OPL, introduzido no Windows Media DRM 10, permite que as licenças sejam criadas com mais flexibilidade do que nas versões anteriores. Você pode especificar as OPLs mínimas necessárias para reprodução e cópia. Além disso, você pode especificar exceções para o OPL mínimo, para permitir que uma tecnologia não seja classificada como alta o suficiente ou para não permitir uma tecnologia com um OPL que exceda o mínimo.

Ao especificar restrições a licenças usando OPLs, um proprietário de conteúdo só precisa usar duas ações (Copiar e Reproduzir), em que as versões anteriores tinham ações separadas definidas para os vários tipos de dispositivos com suporte para cópia (SDMI, não SDMI e CD de áudio do Red Book).

**Observação** O DRM não é suportado pela versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management dados digitais**](digital-rights-management-features.md)
</dt> <dt>

[**Trabalhando com níveis de proteção de saída**](working-with-output-protection-levels.md)
</dt> </dl>

 

 




