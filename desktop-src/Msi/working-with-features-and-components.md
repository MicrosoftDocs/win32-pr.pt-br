---
description: Há várias funções que alteram a instalação dos componentes e recursos do produto. O a seguir descreve como alterar recursos e componentes do.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Trabalhando com recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145169"
---
# <a name="working-with-features-and-components"></a>Trabalhando com recursos e componentes

Há várias funções que alteram a instalação dos [componentes e recursos](components-and-features.md)do produto. O a seguir descreve como alterar recursos e componentes do.

**Para alterar a instalação de recursos e componentes**

1.  Defina o nível de instalação para um componente ou recurso chamando a função [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .

    Cada recurso em um pacote recebe um nível de instalação na [tabela de recursos](feature-table.md). Se o nível de instalação de um recurso for menor do que o nível definido por [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), o recurso será selecionado para instalação. Depois que **MsiSetInstallLevel** for chamado, você poderá alterar explicitamente se um recurso está instalado.

2.  Determine quais Estados estão disponíveis para um recurso especificado chamando a função [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .
3.  Obtenha os requisitos de espaço em disco para um recurso especificado e seus recursos filho chamando a função [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .
4.  Obtenha o estado atual de um recurso ou componente chamando a função [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) ou a função [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .
5.  Altere o estado do recurso ou componente com a função [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) ou a função [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .

 

 



