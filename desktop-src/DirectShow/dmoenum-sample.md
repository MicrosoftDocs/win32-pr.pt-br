---
description: Exemplo de DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Exemplo de DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163858"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="1d4cb-103">Exemplo de DMOEnum</span><span class="sxs-lookup"><span data-stu-id="1d4cb-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="1d4cb-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d4cb-104">Description</span></span>

<span data-ttu-id="1d4cb-105">Esse aplicativo de exemplo enumera todos os DMOS ( [objetos de mídia do DirectX](directx-media-objects.md) ) registrados no sistema do usuário e exibe informações sobre eles.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="1d4cb-106">O exemplo usa a função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e a interface [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) para enumerar o DMOs.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="1d4cb-107">Ele usa a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e outras interfaces DMO para recuperar informações sobre cada DMO.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="1d4cb-108">Uso</span><span class="sxs-lookup"><span data-stu-id="1d4cb-108">Usage</span></span>

<span data-ttu-id="1d4cb-109">Quando o aplicativo é iniciado, ele enumera todos os DMOs instalados.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="1d4cb-110">Se você selecionar uma categoria de DMO específica, o aplicativo exibirá apenas o DMOs nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="1d4cb-111">Para exibir informações sobre um DMO, selecione o DMO na lista.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="1d4cb-112">O aplicativo exibe o número de fluxos, os tipos de mídia preferenciais, o servidor DLL para esse DMO e outras informações sobre o DMO.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="1d4cb-113">Para incluir ou excluir DMOs com chave, alterne a caixa de seleção **incluir DMOs com chave?** .</span><span class="sxs-lookup"><span data-stu-id="1d4cb-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="1d4cb-114">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1d4cb-114">Downloading the Sample</span></span>

<span data-ttu-id="1d4cb-115">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d4cb-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="1d4cb-116">Este exemplo é instalado no seguinte caminho: exemplos de *\[ raiz \] do SDK* \\ \\ multimídia \\ DirectShow \\ misc \\ DMOEnum.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d4cb-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d4cb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d4cb-118">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="1d4cb-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



