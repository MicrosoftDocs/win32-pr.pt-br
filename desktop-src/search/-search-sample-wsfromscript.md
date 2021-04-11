---
description: O exemplo de código WSFromScript demonstra como consultar o Windows Search de um script do Microsoft Visual Basic usando o Microsoft ActiveX Data Objects (ADO).
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: WSFromScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296243"
---
# <a name="wsfromscript"></a><span data-ttu-id="04315-103">WSFromScript</span><span class="sxs-lookup"><span data-stu-id="04315-103">WSFromScript</span></span>

<span data-ttu-id="04315-104">O exemplo de código WSFromScript demonstra como consultar o Windows Search de um script do Microsoft Visual Basic usando o Microsoft ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="04315-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="04315-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="04315-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="04315-106">Requirements</span><span class="sxs-lookup"><span data-stu-id="04315-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="04315-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04315-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="04315-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04315-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="04315-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04315-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="04315-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04315-110">Requirements</span></span>

| <span data-ttu-id="04315-111">Produto</span><span class="sxs-lookup"><span data-stu-id="04315-111">Product</span></span>     | <span data-ttu-id="04315-112">Versão do produto</span><span class="sxs-lookup"><span data-stu-id="04315-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="04315-113">Windows</span><span class="sxs-lookup"><span data-stu-id="04315-113">Windows</span></span>     | <span data-ttu-id="04315-114">no Windows 7, 8.1 ou 10</span><span class="sxs-lookup"><span data-stu-id="04315-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="04315-115">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="04315-115">Windows SDK</span></span> | <span data-ttu-id="04315-116">7,0 ou superior</span><span class="sxs-lookup"><span data-stu-id="04315-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="04315-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04315-117">Downloading the Sample</span></span>

<span data-ttu-id="04315-118">Este exemplo está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="04315-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="04315-119">Local</span><span class="sxs-lookup"><span data-stu-id="04315-119">Location</span></span>      | <span data-ttu-id="04315-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="04315-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="04315-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="04315-121">GitHub</span></span>  | [<span data-ttu-id="04315-122">Exemplo de WSFromScript</span><span class="sxs-lookup"><span data-stu-id="04315-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="04315-123">Para todas as versões do Windows, incluindo o Windows 7, é recomendável baixar os exemplos diretamente do GitHub para obter a versão mais atualizada.</span><span class="sxs-lookup"><span data-stu-id="04315-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="04315-124">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="04315-124">Building the Sample</span></span>

<span data-ttu-id="04315-125">Para criar o exemplo na janela de prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="04315-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="04315-126">Abra a janela do prompt de comando e navegue até o diretório do projeto **QueryEverything** .</span><span class="sxs-lookup"><span data-stu-id="04315-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="04315-127">Por exemplo, o caminho de instalação padrão completo do SDK do Windows 7 é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` .</span><span class="sxs-lookup"><span data-stu-id="04315-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="04315-128">Digite `cscript QueryEverything.vbs`.</span><span class="sxs-lookup"><span data-stu-id="04315-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04315-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="04315-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="04315-130">Conceitual</span><span class="sxs-lookup"><span data-stu-id="04315-130">Conceptual</span></span>

<span data-ttu-id="04315-131">[**Referência da linguagem VBScript**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="04315-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="04315-132">Outros exemplos</span><span class="sxs-lookup"><span data-stu-id="04315-132">Other Samples</span></span>

[<span data-ttu-id="04315-133">Exemplos de código de pesquisa</span><span class="sxs-lookup"><span data-stu-id="04315-133">Search Code Samples</span></span>](-search-samples-ovw.md)
