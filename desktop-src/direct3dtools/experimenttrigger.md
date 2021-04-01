---
description: Representa informações do gatilho de teste.
MS-HAID: vspixengine.ExperimentTrigger
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura ExperimentTrigger
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAA67E5-9C43-4BCD-9388-63EF06AB1C0E
api_name:
- ExperimentTrigger
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bba350657cf738058ecd3f38d7284b72deda1c17
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825728"
---
# <a name="span-idvspixengineexperimenttriggerspanexperimenttrigger-structure"></a><span data-ttu-id="fd3f0-103"><span id="vspixengine.experimenttrigger"></span>Estrutura ExperimentTrigger</span><span class="sxs-lookup"><span data-stu-id="fd3f0-103"><span id="vspixengine.experimenttrigger"></span>ExperimentTrigger structure</span></span>

<span data-ttu-id="fd3f0-104">Representa informações do gatilho de teste.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-104">Represents experiment trigger information.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd3f0-105">Syntax</span></span>


```C++
} ExperimentTrigger;
```

## <a name="members"></a><span data-ttu-id="fd3f0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fd3f0-106">Members</span></span>

<span data-ttu-id="fd3f0-107">**tipo**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-107">**type**</span></span>  
<span data-ttu-id="fd3f0-108">O tipo de experimento (captura) disparado.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-108">The kind of experiment (capture) triggered.</span></span>

<span data-ttu-id="fd3f0-109">**chave**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-109">**key**</span></span>  
<span data-ttu-id="fd3f0-110">Quando Type é igual a EXPERIMENTTRIGGERTYPE:: KEY, a chave usada para disparar a captura.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-110">When type is equal to EXPERIMENTTRIGGERTYPE::KEY, the key used to trigger capture.</span></span>

<span data-ttu-id="fd3f0-111">**frameNumber**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-111">**frameNumber**</span></span>  
<span data-ttu-id="fd3f0-112">Quando Type é igual a EXPERIMENTTRIGGERTYPE:: FRAMENUMBER, o número do quadro que irá disparar a captura.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-112">When type is equal to EXPERIMENTTRIGGERTYPE::FRAMENUMBER, the frame number that will trigger capture.</span></span>

<span data-ttu-id="fd3f0-113">**captureCount**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-113">**captureCount**</span></span>  
<span data-ttu-id="fd3f0-114">O número de quadros sequenciais a serem capturados.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-114">The number of sequential frames to capture.</span></span>

<span data-ttu-id="fd3f0-115">**actionIID**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-115">**actionIID**</span></span>  
<span data-ttu-id="fd3f0-116">A ID do evento de ação (captura de tela, captura de quadros, etc.)</span><span class="sxs-lookup"><span data-stu-id="fd3f0-116">The ID of the action event (screenshot, frame capture, etc).</span></span>

<span data-ttu-id="fd3f0-117">**actionPlayload**</span><span class="sxs-lookup"><span data-stu-id="fd3f0-117">**actionPlayload**</span></span>  
<span data-ttu-id="fd3f0-118">Um ponteiro para a carga do evento de ação.</span><span class="sxs-lookup"><span data-stu-id="fd3f0-118">A pointer to the action event payload.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3f0-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fd3f0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd3f0-120">Header</span></span></p></td><td><span data-ttu-id="fd3f0-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fd3f0-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



