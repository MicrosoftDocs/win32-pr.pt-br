---
description: Há várias funções que um aplicativo deve chamar para solicitar recursos.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Solicitando um recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011256"
---
# <a name="requesting-a-feature"></a>Solicitando um recurso

Há várias funções que um aplicativo deve chamar para solicitar recursos. Antes de solicitar um recurso, o aplicativo deve garantir que o recurso esteja instalado. Se o aplicativo chamar [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) antes que o aplicativo acesse um recurso, o aplicativo poderá usar as informações retornadas para manter as métricas de uso.

**Para solicitar um recurso**

1.  Chame o [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ou a função [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se você quiser determinar a disponibilidade de um recurso sem incrementar a contagem de uso.
2.  Indique a intenção do aplicativo de usar um recurso chamando a função [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .
3.  Determine os locais de arquivo chamando a função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .
4.  Configure o recurso chamando a função [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .
5.  Obtenha métricas de uso que seu aplicativo pode usar chamando a função [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .

O diagrama a seguir ilustra o modelo de solicitação de recurso.

![modelo de solicitação de recurso. ](images/over2.png)

 

 



