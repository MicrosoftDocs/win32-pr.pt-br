---
title: Comentários (msfeeds. h)
description: Adicione comentários a metaarquivos seguindo a sintaxe linguagem XML (XML). Os comentários começam com \ 0034; --\ 0034; e terminar com \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Comentários do Windows Media Player
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761117"
---
# <a name="comments-msfeedsh"></a><span data-ttu-id="2a974-105">Comentários (msfeeds. h)</span><span class="sxs-lookup"><span data-stu-id="2a974-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="2a974-106">Adicione comentários a metaarquivos seguindo a sintaxe linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="2a974-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="2a974-107">Os comentários começam com " &lt; !--" e terminam com "-- &gt; ".</span><span class="sxs-lookup"><span data-stu-id="2a974-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="2a974-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a974-108">Remarks</span></span>

<span data-ttu-id="2a974-109">Os comentários podem aparecer em qualquer lugar, exceto no conteúdo do elemento (entre marcas de abertura e fechamento do elemento,  < >).</span><span class="sxs-lookup"><span data-stu-id="2a974-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="2a974-110">Eles não fazem parte dos dados de caracteres do documento e são ignorados quando o metarquivo é analisado.</span><span class="sxs-lookup"><span data-stu-id="2a974-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="2a974-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2a974-111">Examples</span></span>


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a><span data-ttu-id="2a974-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a974-112">Requirements</span></span>



| <span data-ttu-id="2a974-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a974-113">Requirement</span></span> | <span data-ttu-id="2a974-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2a974-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a974-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a974-115">Header</span></span><br/> | <dl> <span data-ttu-id="2a974-116"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a974-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a974-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a974-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a974-118">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="2a974-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





