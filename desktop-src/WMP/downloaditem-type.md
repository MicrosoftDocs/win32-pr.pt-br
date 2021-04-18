---
title: DownloadItem. Type
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A propriedade Type recupera o tipo de download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. digite Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788176"
---
# <a name="downloaditemtype"></a><span data-ttu-id="28b84-106">DownloadItem. Type</span><span class="sxs-lookup"><span data-stu-id="28b84-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="28b84-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="28b84-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="28b84-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="28b84-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="28b84-109">A propriedade **Type** recupera o tipo de download.</span><span class="sxs-lookup"><span data-stu-id="28b84-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b84-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b84-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="28b84-111">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="28b84-111">Possible Values</span></span>

<span data-ttu-id="28b84-112">Essa propriedade é uma **cadeia de caracteres** somente leitura que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="28b84-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="28b84-113">Valor</span><span class="sxs-lookup"><span data-stu-id="28b84-113">Value</span></span>      | <span data-ttu-id="28b84-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="28b84-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b84-115">background</span><span class="sxs-lookup"><span data-stu-id="28b84-115">background</span></span> | <span data-ttu-id="28b84-116">(Somente Windows XP.) O download ocorre como um processo em segundo plano à medida que o tempo do processador se torna disponível.</span><span class="sxs-lookup"><span data-stu-id="28b84-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="28b84-117">Os Estados de download persistem mesmo quando o Windows Media Player ou o Windows XP é desligado.</span><span class="sxs-lookup"><span data-stu-id="28b84-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="28b84-118">em tempo real</span><span class="sxs-lookup"><span data-stu-id="28b84-118">real time</span></span>  | <span data-ttu-id="28b84-119">(Todos os sistemas operacionais com suporte.) O download ocorre de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="28b84-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="28b84-120">Nenhum estado de download persiste entre sessões.</span><span class="sxs-lookup"><span data-stu-id="28b84-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="28b84-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="28b84-121">Remarks</span></span>

<span data-ttu-id="28b84-122">Cada tipo de download tem vantagens e desvantagens.</span><span class="sxs-lookup"><span data-stu-id="28b84-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="28b84-123">O download em segundo plano permite que o usuário prossiga para outras tarefas e até mesmo reinicie o Windows sem cancelar o download, mas leva mais tempo em geral para concluir o download e só tem suporte para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="28b84-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="28b84-124">O download em tempo real leva menos tempo para ser concluído, mas exige que o usuário Conclua todo o download antes de fechar o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="28b84-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b84-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28b84-125">Requirements</span></span>



| <span data-ttu-id="28b84-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b84-126">Requirement</span></span> | <span data-ttu-id="28b84-127">Valor</span><span class="sxs-lookup"><span data-stu-id="28b84-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28b84-128">Versão</span><span class="sxs-lookup"><span data-stu-id="28b84-128">Version</span></span><br/> | <span data-ttu-id="28b84-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="28b84-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="28b84-130">DLL</span><span class="sxs-lookup"><span data-stu-id="28b84-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="28b84-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28b84-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28b84-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="28b84-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b84-133">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="28b84-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





