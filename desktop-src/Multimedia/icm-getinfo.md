---
title: Mensagem de ICM_GETINFO (VFW. h)
description: A \_ mensagem ICM GetInfo consulta um driver de compactação de vídeo para retornar uma descrição de si mesmo em uma estrutura ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- Multimídia do Windows de mensagem ICM_GETINFO
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759628"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="6b653-104">\_Mensagem ICM GETinfo</span><span class="sxs-lookup"><span data-stu-id="6b653-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="6b653-105">A mensagem **ICM \_ GetInfo** consulta um driver de compactação de vídeo para retornar uma descrição de si mesmo em uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="6b653-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="6b653-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b653-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b653-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="6b653-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="6b653-108">Ponteiro para uma estrutura **ICINFO** para conter informações.</span><span class="sxs-lookup"><span data-stu-id="6b653-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="6b653-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b653-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6b653-110">Tamanho, em bytes, de **ICINFO**.</span><span class="sxs-lookup"><span data-stu-id="6b653-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b653-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6b653-111">Return Value</span></span>

<span data-ttu-id="6b653-112">Retorna o tamanho, em bytes, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ou zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="6b653-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="6b653-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b653-113">Remarks</span></span>

<span data-ttu-id="6b653-114">Normalmente, os aplicativos enviam essa mensagem para exibir uma lista dos compactadores instalados.</span><span class="sxs-lookup"><span data-stu-id="6b653-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="6b653-115">O driver deve preencher todos os membros da estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , exceto **szDriver**.</span><span class="sxs-lookup"><span data-stu-id="6b653-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b653-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b653-116">Requirements</span></span>



| <span data-ttu-id="6b653-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b653-117">Requirement</span></span> | <span data-ttu-id="6b653-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6b653-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b653-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b653-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6b653-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b653-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b653-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b653-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6b653-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6b653-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b653-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6b653-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b653-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b653-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b653-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b653-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b653-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b653-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6b653-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="6b653-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





