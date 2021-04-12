---
title: WM/Gêneroid
description: O atributo WM/Gêneroid contém um identificador de gênero compatível com o conteúdo da marca TCON em ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato de mídia do Windows WM/Gêneroid
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104365033"
---
# <a name="wmgenreid"></a><span data-ttu-id="5635d-104">WM/Gêneroid</span><span class="sxs-lookup"><span data-stu-id="5635d-104">WM/GenreID</span></span>

<span data-ttu-id="5635d-105">O atributo **WM/gêneroid** contém um identificador de gênero compatível com o conteúdo da marca Tcon em ID3v2.</span><span class="sxs-lookup"><span data-stu-id="5635d-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="5635d-106">Isso deve conter a ID do gênero entre parênteses, opcionalmente seguido por um refinamento que descreve ainda mais o gênero.</span><span class="sxs-lookup"><span data-stu-id="5635d-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="5635d-107">Para obter mais informações, consulte a especificação ID3v2.</span><span class="sxs-lookup"><span data-stu-id="5635d-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5635d-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="5635d-108">Global Constant</span></span>

<span data-ttu-id="5635d-109">g \_ wszWMGenreID</span><span class="sxs-lookup"><span data-stu-id="5635d-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="5635d-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="5635d-110">Data Type</span></span>

<span data-ttu-id="5635d-111">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="5635d-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5635d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5635d-112">Remarks</span></span>

<span data-ttu-id="5635d-113">O atributo preferencial para especificar um gênero é [**WM/gênero**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="5635d-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="5635d-114">Use-o em preferência a este atributo.</span><span class="sxs-lookup"><span data-stu-id="5635d-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="5635d-115">Se você alterar o **WM/gênero** ou o **WM/gêneroid** em um arquivo MP3, o outro atributo será alterado para coincidir.</span><span class="sxs-lookup"><span data-stu-id="5635d-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="5635d-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5635d-116">Example</span></span>



| <span data-ttu-id="5635d-117">Tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="5635d-117">File type</span></span> | <span data-ttu-id="5635d-118">Valor de exemplo</span><span class="sxs-lookup"><span data-stu-id="5635d-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="5635d-119">Áudio</span><span class="sxs-lookup"><span data-stu-id="5635d-119">Audio</span></span>     | <span data-ttu-id="5635d-120">"(4) Eurodisco"</span><span class="sxs-lookup"><span data-stu-id="5635d-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="5635d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5635d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5635d-122">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="5635d-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




