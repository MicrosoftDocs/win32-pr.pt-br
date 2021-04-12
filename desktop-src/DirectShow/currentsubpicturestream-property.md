---
description: A propriedade CurrentSubpictureStream define ou recupera o fluxo de subimagem atual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propriedade CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500679"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="d255d-103">Propriedade CurrentSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="d255d-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="d255d-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d255d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d255d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d255d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d255d-106">A `CurrentSubpictureStream` propriedade define ou recupera o fluxo de subimagem atual.</span><span class="sxs-lookup"><span data-stu-id="d255d-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="d255d-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d255d-107">Return Value</span></span>

<span data-ttu-id="d255d-108">Retorna um valor inteiro que representa o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d255d-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="d255d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d255d-109">Remarks</span></span>

<span data-ttu-id="d255d-110">Os valores possíveis dessa propriedade são:</span><span class="sxs-lookup"><span data-stu-id="d255d-110">The possible values of this property are:</span></span>



| <span data-ttu-id="d255d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d255d-111">Value</span></span>   | <span data-ttu-id="d255d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d255d-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="d255d-113">0 a 31</span><span class="sxs-lookup"><span data-stu-id="d255d-113">0 to 31</span></span> | <span data-ttu-id="d255d-114">O fluxo de subimagem</span><span class="sxs-lookup"><span data-stu-id="d255d-114">The subpicture stream</span></span>    |
| <span data-ttu-id="d255d-115">63</span><span class="sxs-lookup"><span data-stu-id="d255d-115">63</span></span>      | <span data-ttu-id="d255d-116">Fluxo de baixa taxa de bits sem áudio</span><span class="sxs-lookup"><span data-stu-id="d255d-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="d255d-117">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d255d-117">This property is read/write with no default value.</span></span> <span data-ttu-id="d255d-118">Antes de definir um novo fluxo de subimagem, chame [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para verificar se o fluxo está disponível.</span><span class="sxs-lookup"><span data-stu-id="d255d-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="d255d-119">Definir essa propriedade faz com que a propriedade [**subpictureize**](subpictureon-property.md) seja alternada para **true**.</span><span class="sxs-lookup"><span data-stu-id="d255d-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d255d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d255d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d255d-121">**Subimagem**</span><span class="sxs-lookup"><span data-stu-id="d255d-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="d255d-122">**SubpictureStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="d255d-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



