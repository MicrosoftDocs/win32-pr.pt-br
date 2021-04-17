---
description: Windows Installer funções que retornam dados em um usuário fornecido – o local da memória não deve ser chamado com NULL como o valor do ponteiro.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Passando nulo para funções Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749788"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="7ba97-103">Passando NULL como o argumento das funções Windows Installer</span><span class="sxs-lookup"><span data-stu-id="7ba97-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="7ba97-104">Windows Installer funções que retornam dados em um usuário fornecido – o local da memória não deve ser chamado com NULL como o valor do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="7ba97-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="7ba97-105">Essas funções retornam uma cadeia de caracteres ou retornam dados como ponteiros inteiros, mas retornam valores inconsistentes ao passar NULL como o valor para o argumento de saída.</span><span class="sxs-lookup"><span data-stu-id="7ba97-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="7ba97-106">Não passe nulo como o valor do argumento de saída para qualquer uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="7ba97-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="7ba97-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="7ba97-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="7ba97-108">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="7ba97-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="7ba97-109">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="7ba97-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="7ba97-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="7ba97-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="7ba97-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="7ba97-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="7ba97-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="7ba97-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="7ba97-113">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="7ba97-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="7ba97-114">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="7ba97-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="7ba97-115">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="7ba97-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="7ba97-116">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="7ba97-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="7ba97-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="7ba97-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="7ba97-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="7ba97-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="7ba97-119">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="7ba97-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="7ba97-120">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="7ba97-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



