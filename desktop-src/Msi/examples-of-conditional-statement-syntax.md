---
description: O seguinte fornece algumas instâncias comuns de instruções condicionais. Para obter mais informações, consulte Sintaxe de instrução condicional.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Exemplos de sintaxe de instrução condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921419"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="2cbf9-104">Exemplos de sintaxe de instrução condicional</span><span class="sxs-lookup"><span data-stu-id="2cbf9-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="2cbf9-105">O seguinte fornece algumas instâncias comuns de instruções condicionais.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="2cbf9-106">Para obter mais informações, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2cbf9-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="2cbf9-107">Executar ação na remoção.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-107">Run action on removal.</span></span>

<span data-ttu-id="2cbf9-108">Para obter informações, consulte [ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="2cbf9-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="2cbf9-109">Execute a ação somente se o produto não tiver sido instalado.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="2cbf9-110">Execute a ação somente se o produto for instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="2cbf9-111">Não execute a ação em uma reinstalação.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="2cbf9-112">O termo "&FeatureName = 3" significa que a ação é instalar o recurso local.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="2cbf9-113">O termo "não (! FeatureName = 3) "significa que o recurso não está instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="2cbf9-114">Executar ação somente se o recurso for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="2cbf9-115">Essa condição verifica apenas uma transição do recurso de um estado instalado de local para o estado ausente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="2cbf9-116">Executar ação somente se o componente tiver sido instalado localmente, mas estiver em transição fora do estado.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="2cbf9-117">O termo "? ComponetName = 3 "significa que o componente está instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="2cbf9-118">O termo "$ComponentName = 2" significa que o estado de ação no componente está ausente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="2cbf9-119">O termo "$ComponentName = 4" significa que o estado de ação no componente é executado a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="2cbf9-120">Observe que um estado de ação de advertise não é válido para um componente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="2cbf9-121">Execute a ação somente na reinstalação de um componente.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="2cbf9-122">Executar ação somente quando um patch específico for aplicado.</span><span class="sxs-lookup"><span data-stu-id="2cbf9-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="2cbf9-123">Para obter mais informações, consulte a seção comentários na página de propriedades [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="2cbf9-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



