---
description: O cenário de DAC (controle de acesso dinâmico) habilita a administração de controle de acesso centralizado para cenários de servidor de arquivos corporativo.
ms.assetid: 5A06B8D8-F14B-4D9E-9ED6-4246A26BF945
title: Política de autorização centralizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a07730bff997b545285b0d2845547a4d5deaffe78324e354e7eecbf879b763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783180"
---
# <a name="centralized-authorization-policy"></a>Política de autorização centralizada

O [cenário de DAC (controle de acesso dinâmico)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) habilita a administração de controle de acesso centralizado para cenários de servidor de arquivos corporativo. A maioria das organizações tem várias áreas nas quais desejam controlar o acesso.

Os exemplos são:

-   Controlando o acesso a informações confidenciais, em que os arquivos marcados como confidenciais teriam permissões específicas
-   Controlando o acesso a arquivos que contêm informações de identificação pessoal (PII)
-   Limitação do acesso a documentos com base nas políticas de retenção das organizações.

Várias novas abstrações de diretiva de autorização são fornecidas para permitir que um administrador defina essas políticas de forma centralizada e simplifique o processo de definição, permitindo que cada um desses requisitos de acesso seja definido e mantido separadamente, mas aplicado como uma política.

Dois novos objetos de política Active Directory, uma Cap ( [política de autorização central](central-authorization-policies.md) ) e uma capr ( [regra de política de autorização central](central-authorization-policy-rule.md) ) são introduzidos no Windows 8 para definir e aplicar políticas de autorização centralizadas com base em expressões de declarações e atributos de recursos. ao usar esses objetos, um administrador define um capr como uma política de autorização específica que pode ser aplicada a recursos que têm um determinado atributo ou atendem a uma determinada condição de aplicabilidade. por exemplo, documentos rotulados como "alto impacto nos negócios". o CAPES pode ser definido para cada política de controle de acesso desejada em uma organização que pode ser expressa, e os recursos aos quais ele deve ser aplicado podem ser identificados, em termos de expressões de DAC do Windows 8. um Cap é uma coleção de caprs que pode ser aplicada em conjunto em recursos. o diagrama a seguir mostra as relações do limite e do cabo e as etapas conceituais envolvidas na definição e aplicação desses objetos aos recursos de arquivo. ![relação de CAPES e Caps](images/cap.png)

 

 
