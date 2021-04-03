---
description: Representa informações sobre um experimento (captura).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura do experimento
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645885"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="d6482-103"><span id="vspixengine.experiment"></span>Estrutura do experimento</span><span class="sxs-lookup"><span data-stu-id="d6482-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="d6482-104">Representa informações sobre um experimento (captura).</span><span class="sxs-lookup"><span data-stu-id="d6482-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6482-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6482-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="d6482-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d6482-106">Members</span></span>

<span data-ttu-id="d6482-107">**processId**</span><span class="sxs-lookup"><span data-stu-id="d6482-107">**processId**</span></span>  
<span data-ttu-id="d6482-108">A ID do processo associado.</span><span class="sxs-lookup"><span data-stu-id="d6482-108">The associated process ID.</span></span>

<span data-ttu-id="d6482-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="d6482-109">**applicationName**</span></span>  
<span data-ttu-id="d6482-110">Uma cadeia de caracteres COM que contém o nome do aplicativo no qual executar o experimento.</span><span class="sxs-lookup"><span data-stu-id="d6482-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="d6482-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="d6482-111">**commandLineArguments**</span></span>  
<span data-ttu-id="d6482-112">Uma cadeia de caracteres COM que contém os argumentos de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d6482-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="d6482-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="d6482-113">**workingDirectory**</span></span>  
<span data-ttu-id="d6482-114">Uma cadeia de caracteres COM que contém o caminho do diretório de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d6482-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="d6482-115">**tempPixRunFile**</span><span class="sxs-lookup"><span data-stu-id="d6482-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="d6482-116">Uma cadeia de caracteres COM que contém o caminho de arquivo temporário usado para executar o experimento.</span><span class="sxs-lookup"><span data-stu-id="d6482-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="d6482-117">**startOption**</span><span class="sxs-lookup"><span data-stu-id="d6482-117">**startOption**</span></span>  
<span data-ttu-id="d6482-118">A opção start associada ao experimento.</span><span class="sxs-lookup"><span data-stu-id="d6482-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="d6482-119">**experimentotype**</span><span class="sxs-lookup"><span data-stu-id="d6482-119">**experimentType**</span></span>  
<span data-ttu-id="d6482-120">O tipo de experimento (captura).</span><span class="sxs-lookup"><span data-stu-id="d6482-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="d6482-121">**uiLocale**</span><span class="sxs-lookup"><span data-stu-id="d6482-121">**uiLocale**</span></span>  
<span data-ttu-id="d6482-122">A ID da localidade usada para elementos de sobreposição da interface do usuário durante o experiement (captura).</span><span class="sxs-lookup"><span data-stu-id="d6482-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="d6482-123">Isso é passado do host (como o Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="d6482-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="d6482-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="d6482-124">**registryRoot**</span></span>  
<span data-ttu-id="d6482-125">Uma cadeia de caracteres COM que contém a raiz do registro.</span><span class="sxs-lookup"><span data-stu-id="d6482-125">A COM string containing the registry root.</span></span> <span data-ttu-id="d6482-126">Isso é passado do host (como o Visual Studio Diagnóstico de Gráficos) para o mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="d6482-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6482-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6482-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d6482-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6482-128">Header</span></span></p></td><td><span data-ttu-id="d6482-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d6482-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



