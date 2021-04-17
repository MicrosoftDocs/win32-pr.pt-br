---
description: Uma estrutura que descreve um único valor de cor.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785308"
---
# <a name="xps_color"></a><span data-ttu-id="a05d2-103">cor do XPS \_</span><span class="sxs-lookup"><span data-stu-id="a05d2-103">XPS\_COLOR</span></span>

<span data-ttu-id="a05d2-104">Uma estrutura que descreve um único valor de cor.</span><span class="sxs-lookup"><span data-stu-id="a05d2-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="a05d2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a05d2-105">Remarks</span></span>

<span data-ttu-id="a05d2-106">O formato da estrutura depende do valor de *ColorType*.</span><span class="sxs-lookup"><span data-stu-id="a05d2-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="a05d2-107">[**\_tipo de cor XPS \_ \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a05d2-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="a05d2-108">[**\_tipo de cor XPS \_ \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a05d2-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="a05d2-109">**\_contexto de \_ tipo de cor XPS \_**</span><span class="sxs-lookup"><span data-stu-id="a05d2-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="a05d2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a05d2-110">Requirements</span></span>



| <span data-ttu-id="a05d2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a05d2-111">Requirement</span></span> | <span data-ttu-id="a05d2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a05d2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a05d2-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a05d2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a05d2-114">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a05d2-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="a05d2-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a05d2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a05d2-116">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a05d2-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a05d2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a05d2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05d2-118"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="a05d2-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="a05d2-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="a05d2-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a05d2-120"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a05d2-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="a05d2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a05d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05d2-122">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="a05d2-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

