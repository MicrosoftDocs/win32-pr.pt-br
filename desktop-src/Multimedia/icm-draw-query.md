---
title: Mensagem de ICM_DRAW_QUERY (VFW. h)
description: A \_ mensagem de consulta de desenho ICM \_ consulta um driver de renderização para determinar se ele pode renderizar dados em um formato específico. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_QUERY
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455326"
---
# <a name="icm_draw_query-message"></a><span data-ttu-id="9ef3a-105">Mensagem de consulta de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="9ef3a-105">ICM\_DRAW\_QUERY message</span></span>

<span data-ttu-id="9ef3a-106">A mensagem de **\_ \_ consulta de desenho ICM** consulta um driver de renderização para determinar se ele pode renderizar dados em um formato específico.</span><span class="sxs-lookup"><span data-stu-id="9ef3a-106">The **ICM\_DRAW\_QUERY** message queries a rendering driver to determine if it can render data in a specific format.</span></span> <span data-ttu-id="9ef3a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .</span><span class="sxs-lookup"><span data-stu-id="9ef3a-107">You can send this message explicitly or by using the [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) macro.</span></span>


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="9ef3a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ef3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ef3a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="9ef3a-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="9ef3a-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="9ef3a-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ef3a-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9ef3a-111">Return Value</span></span>

<span data-ttu-id="9ef3a-112">Retornará ICERR \_ OK se o driver puder renderizar dados no formato especificado ou ICERR \_ BADFORMAT de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9ef3a-112">Returns ICERR\_OK if the driver can render data in the specified format or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ef3a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ef3a-113">Remarks</span></span>

<span data-ttu-id="9ef3a-114">Essa mensagem é diferente da mensagem [**ICM \_ draw \_ begin**](icm-draw-begin.md) , pois consulta o driver em um sentido geral.</span><span class="sxs-lookup"><span data-stu-id="9ef3a-114">This message differs from the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message in that it queries the driver in a general sense.</span></span> <span data-ttu-id="9ef3a-115">**ICM \_ O DRAW \_ begin** determina se o driver pode desenhar os dados usando o formato especificado sob condições específicas, como esticar a imagem.</span><span class="sxs-lookup"><span data-stu-id="9ef3a-115">**ICM\_DRAW\_BEGIN** determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ef3a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ef3a-116">Requirements</span></span>



| <span data-ttu-id="9ef3a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ef3a-117">Requirement</span></span> | <span data-ttu-id="9ef3a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9ef3a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9ef3a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ef3a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ef3a-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ef3a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9ef3a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ef3a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ef3a-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ef3a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9ef3a-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ef3a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ef3a-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ef3a-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ef3a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ef3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ef3a-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ef3a-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="9ef3a-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="9ef3a-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

