---
description: 'Há quatro camadas para a biblioteca de análise de tinta: Windows Forms, WPF, COM e a camada base. Esta seção descreve quando usar cada camada.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso da API de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920744"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="b1946-104">Uso da API de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b1946-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="b1946-105">Há quatro camadas para a biblioteca de análise de tinta: Windows Forms, WPF, COM e a camada base.</span><span class="sxs-lookup"><span data-stu-id="b1946-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="b1946-106">Esta seção descreve quando usar cada camada.</span><span class="sxs-lookup"><span data-stu-id="b1946-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="b1946-107">Visão geral da API de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b1946-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="b1946-108">As bibliotecas de análise de tinta são projetadas para serem usadas em uma variedade de ambientes de programação com suporte.</span><span class="sxs-lookup"><span data-stu-id="b1946-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="b1946-109">Há quatro camadas básicas por meio das quais seu aplicativo pode fazer uso da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="b1946-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="b1946-110">Essas camadas são:</span><span class="sxs-lookup"><span data-stu-id="b1946-110">These layers are:</span></span>

-   <span data-ttu-id="b1946-111">A camada de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b1946-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="b1946-112">A camada do WPF</span><span class="sxs-lookup"><span data-stu-id="b1946-112">The WPF layer</span></span>
-   <span data-ttu-id="b1946-113">A camada COM</span><span class="sxs-lookup"><span data-stu-id="b1946-113">The COM layer</span></span>
-   <span data-ttu-id="b1946-114">A camada base</span><span class="sxs-lookup"><span data-stu-id="b1946-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="b1946-115">Aplicativos do Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b1946-115">Windows Forms Applications</span></span>

<span data-ttu-id="b1946-116">Você pode usar a API de análise de tinta em seu projeto gerenciado adicionando uma referência às seguintes bibliotecas:</span><span class="sxs-lookup"><span data-stu-id="b1946-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="b1946-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="b1946-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="b1946-118">Biblioteca de análise de documento de tinta (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="b1946-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="b1946-119">Em Windows Forms aplicativos, você provavelmente usará as bibliotecas em conjunto com os objetos de plataforma do Tablet PC padrão encontrados no assembly do Microsoft Tablet PC API v 1.7.</span><span class="sxs-lookup"><span data-stu-id="b1946-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="b1946-120">Verifique também se você tem uma referência para:</span><span class="sxs-lookup"><span data-stu-id="b1946-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="b1946-121">Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="b1946-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="b1946-122">Aplicativos do Windows Presentation Framework</span><span class="sxs-lookup"><span data-stu-id="b1946-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="b1946-123">Você pode usar a API de análise de tinta em seu projeto do WPF adicionando uma referência aos membros da análise de tinta que são definidos no namespace System. Windows. Ink no assembly IAWinFX.dll.</span><span class="sxs-lookup"><span data-stu-id="b1946-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="b1946-124">Esse assembly é instalado pelo SDK.</span><span class="sxs-lookup"><span data-stu-id="b1946-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="b1946-125">Aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="b1946-125">COM Applications</span></span>

<span data-ttu-id="b1946-126">Aplicativos COM não automação devem usar a camada COM das APIs de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="b1946-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="b1946-127">Digite objetos [ContextNode](/previous-versions/ms551996(v=vs.100)) específicos-como [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))e outros-não são usados na camada com.</span><span class="sxs-lookup"><span data-stu-id="b1946-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="b1946-128">Em vez disso, você deve usar [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) na interface [**IContextNode**](icontextnode.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="b1946-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="b1946-129">Você deve \# incluir "IACom. h".</span><span class="sxs-lookup"><span data-stu-id="b1946-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="b1946-130">Você provavelmente usará as bibliotecas em conjunto com o objeto de tinta da plataforma Tablet PC; portanto, você também deve \# incluir "msinkaut. h".</span><span class="sxs-lookup"><span data-stu-id="b1946-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="b1946-131">RTS e outros aplicativos</span><span class="sxs-lookup"><span data-stu-id="b1946-131">RTS and Other Applications</span></span>

<span data-ttu-id="b1946-132">A camada base de análise de tinta funciona de forma diferente das outras, pois ela leva dados de ponto para análise em vez de objetos [Stroke](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="b1946-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="b1946-133">Exemplos de onde você trabalharia com a camada base diretamente em vez de usar as camadas Windows Forms ou COM incluem aplicativos que não usam a primeira geração de objetos de tinta da plataforma Tablet PC ou aplicativos que usam as APIs do [**RealTimeStylus**](realtimestylus-class.md) para gerenciar a entrada de caneta em vez de usar os objetos de [tinta](/previous-versions/ms583670(v=vs.100)) da plataforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b1946-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="b1946-134">Somente suporte de 32 bits</span><span class="sxs-lookup"><span data-stu-id="b1946-134">32-bit Support Only</span></span>

<span data-ttu-id="b1946-135">Observe que as bibliotecas de análise de tinta só têm suporte em processos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b1946-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1946-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1946-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1946-137">Visão geral da análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b1946-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="b1946-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b1946-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
