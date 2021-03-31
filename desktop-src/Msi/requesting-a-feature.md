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
# <a name="requesting-a-feature"></a><span data-ttu-id="2a62b-103">Solicitando um recurso</span><span class="sxs-lookup"><span data-stu-id="2a62b-103">Requesting a Feature</span></span>

<span data-ttu-id="2a62b-104">Há várias funções que um aplicativo deve chamar para solicitar recursos.</span><span class="sxs-lookup"><span data-stu-id="2a62b-104">There are several functions an application must call to request features.</span></span> <span data-ttu-id="2a62b-105">Antes de solicitar um recurso, o aplicativo deve garantir que o recurso esteja instalado.</span><span class="sxs-lookup"><span data-stu-id="2a62b-105">Before requesting a feature, the application must ensure that the feature is installed.</span></span> <span data-ttu-id="2a62b-106">Se o aplicativo chamar [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) antes que o aplicativo acesse um recurso, o aplicativo poderá usar as informações retornadas para manter as métricas de uso.</span><span class="sxs-lookup"><span data-stu-id="2a62b-106">If the application calls [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) before the application accesses a feature, the application can use the information returned to maintain usage metrics.</span></span>

<span data-ttu-id="2a62b-107">**Para solicitar um recurso**</span><span class="sxs-lookup"><span data-stu-id="2a62b-107">**To request a feature**</span></span>

1.  <span data-ttu-id="2a62b-108">Chame o [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) ou a função [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) se você quiser determinar a disponibilidade de um recurso sem incrementar a contagem de uso.</span><span class="sxs-lookup"><span data-stu-id="2a62b-108">Call the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) or the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function if you want to determine the availability of a feature without incrementing the usage count.</span></span>
2.  <span data-ttu-id="2a62b-109">Indique a intenção do aplicativo de usar um recurso chamando a função [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="2a62b-109">Indicate your application's intent to use a feature by calling the [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) function.</span></span>
3.  <span data-ttu-id="2a62b-110">Determine os locais de arquivo chamando a função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) .</span><span class="sxs-lookup"><span data-stu-id="2a62b-110">Determine file locations by calling the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>
4.  <span data-ttu-id="2a62b-111">Configure o recurso chamando a função [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) .</span><span class="sxs-lookup"><span data-stu-id="2a62b-111">Configure the feature by calling the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) function.</span></span>
5.  <span data-ttu-id="2a62b-112">Obtenha métricas de uso que seu aplicativo pode usar chamando a função [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) .</span><span class="sxs-lookup"><span data-stu-id="2a62b-112">Obtain usage metrics that your application can use by calling the [**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) function.</span></span>

<span data-ttu-id="2a62b-113">O diagrama a seguir ilustra o modelo de solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="2a62b-113">The following diagram illustrates the feature request model.</span></span>

![<span data-ttu-id="2a62b-114">modelo de solicitação de recurso.</span><span class="sxs-lookup"><span data-stu-id="2a62b-114">feature request model.</span></span> ](images/over2.png)

 

 



