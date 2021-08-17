---
description: A API do Provedor de Rede especifica uma única função de funcionalidades.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funções de funcionalidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141269"
---
# <a name="capabilities-functions"></a>Funções de funcionalidades

A API do Provedor de Rede especifica uma única função de funcionalidades. Quando o sistema operacional solicita informações sobre os recursos de um provedor de rede, o MPR [*(Roteador*](/windows/desktop/SecGloss/m-gly) De Vários Provedores) chama a [**função NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada provedor de rede cuja rede está ativa.

A [**função NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) retorna uma máscara de bits que indica quais funções da API do Provedor de Rede o provedor de rede dá suporte. A **função NPGetCaps** é a única função que um provedor de rede deve implementar. O sistema operacional chama essa função para determinar a quais outras funções da API do Provedor de Rede o provedor dá suporte.

 

 
