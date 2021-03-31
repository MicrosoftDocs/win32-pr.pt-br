---
title: Níveis de proteção de saída
description: Níveis de proteção de saída
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- SDK do Windows Media Format, níveis de proteção de saída (OPL)
- DRM (gerenciamento de direitos digitais), OPL (níveis de proteção de saída)
- DRM (gerenciamento de direitos digitais), níveis de proteção de saída (OPL)
- níveis de proteção de saída (OPL)
- OPL (níveis de proteção de saída)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916036"
---
# <a name="output-protection-levels"></a>Níveis de proteção de saída

Os níveis de proteção de saída (OPLs) são classificações numéricas associadas a várias tecnologias que recebem conteúdo de mídia digital. O nível a que a tecnologia dá suporte depende de quão segura ela é. O sistema OPL, introduzido no Windows Media DRM 10, permite que as licenças sejam criadas com mais flexibilidade do que nas versões anteriores. Você pode especificar o mínimo de OPLs necessário para reprodução e para cópia. Além disso, você pode especificar exceções para o mínimo de OPL, para permitir que uma tecnologia não seja classificada como alta o suficiente ou para não permitir uma tecnologia com um OPL que exceda o mínimo.

Ao especificar restrições para licenças usando OPLs, um proprietário de conteúdo precisa usar apenas duas ações (copiar e reproduzir), em que as versões anteriores tinham ações separadas definidas para os vários tipos de dispositivos com suporte para cópia (SDMI, não SDMI e CD de áudio de livro vermelho).

**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Trabalhando com níveis de proteção de saída**](working-with-output-protection-levels.md)
</dt> </dl>

 

 




