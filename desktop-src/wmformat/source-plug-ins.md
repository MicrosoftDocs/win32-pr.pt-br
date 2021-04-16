---
title: Plug-ins de origem
description: Plug-ins de origem
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- SDK do Windows Media Format, plug-ins de origem
- ASF (Advanced Systems Format), plug-ins de origem
- ASF (formato de sistemas avançados), plug-ins de origem
- plug-ins de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105772670"
---
# <a name="source-plug-ins"></a><span data-ttu-id="96284-107">Plug-ins de origem</span><span class="sxs-lookup"><span data-stu-id="96284-107">Source Plug-ins</span></span>

<span data-ttu-id="96284-108">Um plug-in de origem é uma opção disponível para os desenvolvedores que desejam implementar seu próprio sistema de armazenamento para arquivos do Windows Media®.</span><span class="sxs-lookup"><span data-stu-id="96284-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="96284-109">Um plug-in de origem permite isso por meio da implementação de uma interface COM chamada **IStream**, que é uma interface padrão para fornecer dados.</span><span class="sxs-lookup"><span data-stu-id="96284-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="96284-110">O plug-in de origem deve ser gravado como uma dll e sua presença é conhecida pelo SDK por meio de uma entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="96284-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="96284-111">Pode haver qualquer número de plug-ins de origem implementados dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="96284-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="96284-112">O plug-in de origem deve exportar a função [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .</span><span class="sxs-lookup"><span data-stu-id="96284-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="96284-113">Para registrar um plug-in de origem, a seguinte entrada de registro deve ser adicionada:</span><span class="sxs-lookup"><span data-stu-id="96284-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="96284-114">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources</span><span class="sxs-lookup"><span data-stu-id="96284-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="96284-115">Name = "qualquer nome exclusivo"</span><span class="sxs-lookup"><span data-stu-id="96284-115">Name = "any unique name"</span></span>

<span data-ttu-id="96284-116">Valor = nome do caminho da DLL de plug-in de origem</span><span class="sxs-lookup"><span data-stu-id="96284-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="96284-117">Depois que a DLL tiver sido registrada, o aplicativo poderá usar o método **IWMReader:: Open** (com a URL apropriada como um parâmetro) para acessar dados de fluxo, que podem ser armazenados em arquivos ou contêineres de dados definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="96284-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96284-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96284-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96284-119">**IWMReader:: abrir**</span><span class="sxs-lookup"><span data-stu-id="96284-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="96284-120">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="96284-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="96284-121">**WMCreateStreamForURL**</span><span class="sxs-lookup"><span data-stu-id="96284-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




