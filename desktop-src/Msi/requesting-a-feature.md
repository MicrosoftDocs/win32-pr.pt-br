---
description: Há várias funções que um aplicativo deve chamar para solicitar recursos.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Solicitando um recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288804168f6adf936550fee0ac0c542bd68f4d468d6aedd6372071744b9fec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990551"
---
# <a name="requesting-a-feature"></a>Solicitando um recurso

Há várias funções que um aplicativo deve chamar para solicitar recursos. Antes de solicitar um recurso, o aplicativo deve garantir que o recurso está instalado. Se o aplicativo chamar [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) antes de o aplicativo acessar um recurso, o aplicativo poderá usar as informações retornadas para manter as métricas de uso.

**Para solicitar um recurso**

1.  Chame a [**função MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ou [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se você quiser determinar a disponibilidade de um recurso sem incrementar a contagem de uso.
2.  Indique a intenção do aplicativo de usar um recurso chamando a [**função MsiUseFeature.**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
3.  Determine os locais de arquivo chamando a [**função MsiGetComponentPath.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
4.  Configure o recurso chamando a [**função MsiConfigureFeature.**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
5.  Obtenha métricas de uso que seu aplicativo pode usar chamando a [**função MsiGetFeatureUsage.**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)

O diagrama a seguir ilustra o modelo de solicitação de recurso.

![modelo de solicitação de recurso. ](images/over2.png)

 

 



