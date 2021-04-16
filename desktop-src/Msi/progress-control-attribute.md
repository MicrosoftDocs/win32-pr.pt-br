---
description: Esse atributo mede a distância em que a barra de indicadores de progresso é preenchida.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Atributo de controle de progresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750604"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="f779f-103">Atributo de controle de progresso</span><span class="sxs-lookup"><span data-stu-id="f779f-103">Progress Control Attribute</span></span>

<span data-ttu-id="f779f-104">Esse atributo mede a distância em que a barra de indicadores de progresso é preenchida.</span><span class="sxs-lookup"><span data-stu-id="f779f-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="f779f-105">O registro contém dois inteiros e uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f779f-105">The record contains two integers and a string.</span></span> <span data-ttu-id="f779f-106">O primeiro número é o andamento, o segundo número é o intervalo (o número máximo possível para o andamento).</span><span class="sxs-lookup"><span data-stu-id="f779f-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="f779f-107">Na configuração, os inteiros podem ser inseridos como campos inteiros ou cadeias de caracteres que contêm os inteiros.</span><span class="sxs-lookup"><span data-stu-id="f779f-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="f779f-108">Se o segundo número estiver ausente, supõe-se que seja o padrão (1024).</span><span class="sxs-lookup"><span data-stu-id="f779f-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="f779f-109">Se o progresso for maior do que o intervalo, ele será alterado para ser o intervalo.</span><span class="sxs-lookup"><span data-stu-id="f779f-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="f779f-110">O terceiro campo é uma cadeia de caracteres, o nome da ação cujo progresso é exibido.</span><span class="sxs-lookup"><span data-stu-id="f779f-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="f779f-111">Para obter informações relacionadas, consulte [criando um controle ProgressBar](authoring-a-progressbar-control.md)e [adicionando ações personalizadas ao ProgressBar](adding-custom-actions-to-the-progressbar.md).</span><span class="sxs-lookup"><span data-stu-id="f779f-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="f779f-112">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="f779f-112">Valid Controls</span></span>

[<span data-ttu-id="f779f-113">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="f779f-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="f779f-114">Sinalizadores de bits associados</span><span class="sxs-lookup"><span data-stu-id="f779f-114">Associated Bit Flags</span></span>

<span data-ttu-id="f779f-115">Este atributo não usa sinalizadores de bit.</span><span class="sxs-lookup"><span data-stu-id="f779f-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="f779f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f779f-116">Remarks</span></span>

<span data-ttu-id="f779f-117">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="f779f-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



