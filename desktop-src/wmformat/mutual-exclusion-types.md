---
title: Tipos de exclusão mútua
description: Tipos de exclusão mútua
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- SDK do Windows Media Format, exclusão mútua
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- exclusão mútua, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007072"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="0f3d7-107">Tipos de exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="0f3d7-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="0f3d7-108">Você pode usar tipos de exclusão mútua para identificar a natureza de um objeto de exclusão mútua em um perfil.</span><span class="sxs-lookup"><span data-stu-id="0f3d7-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="0f3d7-109">Os tipos de exclusão mútua são usados como parâmetros para [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) e [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="0f3d7-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="0f3d7-110">A tabela a seguir lista os identificadores para tipos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="0f3d7-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="0f3d7-111">Constante de tipo de exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="0f3d7-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="0f3d7-112">GUID</span><span class="sxs-lookup"><span data-stu-id="0f3d7-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="0f3d7-113">\_Linguagem WMMUTEX do CLSID \_</span><span class="sxs-lookup"><span data-stu-id="0f3d7-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="0f3d7-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="0f3d7-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="0f3d7-115">\_Taxa de \_ bits WMMUTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="0f3d7-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="0f3d7-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="0f3d7-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="0f3d7-117">Apresentação do CLSID \_ WMMUTEX \_</span><span class="sxs-lookup"><span data-stu-id="0f3d7-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="0f3d7-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="0f3d7-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="0f3d7-119">CLSID \_ WMMUTEX \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="0f3d7-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="0f3d7-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="0f3d7-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0f3d7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f3d7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f3d7-122">**Valores GUID**</span><span class="sxs-lookup"><span data-stu-id="0f3d7-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




