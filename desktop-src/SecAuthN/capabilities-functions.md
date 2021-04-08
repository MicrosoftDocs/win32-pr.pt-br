---
description: A API do provedor de rede especifica uma única função de recursos.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funções de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010774"
---
# <a name="capabilities-functions"></a>Funções de recursos

A API do provedor de rede especifica uma única função de recursos. Quando o sistema operacional solicita informações sobre os recursos de um provedor de rede, o MPR ( [*roteador de vários provedores*](/windows/desktop/SecGloss/m-gly) ) chama a função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada provedor de rede cuja rede está ativa.

A função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) retorna um bitmask que indica a quais funções da API do provedor de rede o provedor de rede dá suporte. A função **NPGetCaps** é a única função que um provedor de rede deve implementar. O sistema operacional chama essa função para determinar a quais outras funções da API do provedor de rede o provedor dá suporte.

 

 
