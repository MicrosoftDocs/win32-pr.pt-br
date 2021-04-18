---
description: Há várias funções que alteram a instalação dos componentes e recursos do produto. O a seguir descreve como alterar recursos e componentes do.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Trabalhando com recursos e componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778550"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="04aaa-104">Trabalhando com recursos e componentes</span><span class="sxs-lookup"><span data-stu-id="04aaa-104">Working with Features and Components</span></span>

<span data-ttu-id="04aaa-105">Há várias funções que alteram a instalação dos [componentes e recursos](components-and-features.md)do produto.</span><span class="sxs-lookup"><span data-stu-id="04aaa-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="04aaa-106">O a seguir descreve como alterar recursos e componentes do.</span><span class="sxs-lookup"><span data-stu-id="04aaa-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="04aaa-107">**Para alterar a instalação de recursos e componentes**</span><span class="sxs-lookup"><span data-stu-id="04aaa-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="04aaa-108">Defina o nível de instalação para um componente ou recurso chamando a função [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .</span><span class="sxs-lookup"><span data-stu-id="04aaa-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="04aaa-109">Cada recurso em um pacote recebe um nível de instalação na [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="04aaa-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="04aaa-110">Se o nível de instalação de um recurso for menor do que o nível definido por [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), o recurso será selecionado para instalação.</span><span class="sxs-lookup"><span data-stu-id="04aaa-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="04aaa-111">Depois que **MsiSetInstallLevel** for chamado, você poderá alterar explicitamente se um recurso está instalado.</span><span class="sxs-lookup"><span data-stu-id="04aaa-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="04aaa-112">Determine quais Estados estão disponíveis para um recurso especificado chamando a função [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .</span><span class="sxs-lookup"><span data-stu-id="04aaa-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="04aaa-113">Obtenha os requisitos de espaço em disco para um recurso especificado e seus recursos filho chamando a função [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .</span><span class="sxs-lookup"><span data-stu-id="04aaa-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="04aaa-114">Obtenha o estado atual de um recurso ou componente chamando a função [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) ou a função [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="04aaa-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="04aaa-115">Altere o estado do recurso ou componente com a função [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) ou a função [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="04aaa-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



