---
title: WM/WMContentID
description: O atributo WM/WMContentID contém um GUID que identifica o conteúdo.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato de mídia do Windows do WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364903"
---
# <a name="wmwmcontentid"></a><span data-ttu-id="a4657-104">WM/WMContentID</span><span class="sxs-lookup"><span data-stu-id="a4657-104">WM/WMContentID</span></span>

<span data-ttu-id="a4657-105">O atributo **WM/WMContentID** contém um GUID que identifica o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a4657-105">The **WM/WMContentID** attribute contains a GUID identifying the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a4657-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="a4657-106">Global Constant</span></span>

<span data-ttu-id="a4657-107">g \_ wszWMWMContentID</span><span class="sxs-lookup"><span data-stu-id="a4657-107">g\_wszWMWMContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="a4657-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="a4657-108">Data Type</span></span>

<span data-ttu-id="a4657-109">**\_GUID do tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a4657-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4657-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4657-110">Remarks</span></span>

<span data-ttu-id="a4657-111">O conteúdo é identificado pelas tecnologias de mídia do Windows usando três valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**.</span><span class="sxs-lookup"><span data-stu-id="a4657-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="a4657-112">Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence.</span><span class="sxs-lookup"><span data-stu-id="a4657-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="a4657-113">Todos esses três valores são preenchidos pelo Windows Media Player quando os metadados para o conteúdo são recuperados.</span><span class="sxs-lookup"><span data-stu-id="a4657-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="a4657-114">Você pode fazer com que seu aplicativo registre esses valores e usá-los para identificar conteúdo, mas você não deve alterá-los se estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="a4657-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4657-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4657-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4657-116">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="a4657-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




