---
title: WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID contém o GUID da classe de mídia primária.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato de mídia do Windows do WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823349"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="bd585-104">WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="bd585-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="bd585-105">O atributo **WM/MediaClassPrimaryID** contém o GUID da classe de mídia primária.</span><span class="sxs-lookup"><span data-stu-id="bd585-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="bd585-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="bd585-106">Global Constant</span></span>

<span data-ttu-id="bd585-107">g \_ wszWMMediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="bd585-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="bd585-108">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="bd585-108">Data Type</span></span>

<span data-ttu-id="bd585-109">**\_GUID do tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="bd585-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="bd585-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd585-110">Remarks</span></span>

<span data-ttu-id="bd585-111">Esse atributo deve ser definido como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd585-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="bd585-112">GUID de classe primária</span><span class="sxs-lookup"><span data-stu-id="bd585-112">Primary class GUID</span></span>                     | <span data-ttu-id="bd585-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd585-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bd585-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="bd585-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="bd585-115">Use para arquivos de música.</span><span class="sxs-lookup"><span data-stu-id="bd585-115">Use for music files.</span></span> <span data-ttu-id="bd585-116">Não use para áudio que não seja música.</span><span class="sxs-lookup"><span data-stu-id="bd585-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="bd585-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="bd585-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="bd585-118">Use para arquivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bd585-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="bd585-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="bd585-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="bd585-120">Use para arquivos de áudio que não são música.</span><span class="sxs-lookup"><span data-stu-id="bd585-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="bd585-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="bd585-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="bd585-122">Use para arquivos que não são áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="bd585-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="bd585-123">Ao especificar um identificador de classe primário, você também deve definir um identificador de classe secundário para esclarecer o tipo de conteúdo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="bd585-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd585-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd585-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd585-125">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="bd585-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="bd585-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="bd585-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




