---
title: Mensagem de ICM_DECOMPRESSEX_QUERY (VFW. h)
description: A mensagem de consulta DECOMPRESSEX do ICM consulta \_ \_ um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX_QUERY
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824656"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="5b28e-104">\_Mensagem de \_ consulta ICM DECOMPRESSEX</span><span class="sxs-lookup"><span data-stu-id="5b28e-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="5b28e-105">A mensagem de **\_ \_ consulta DECOMPRESSEX do ICM** consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.</span><span class="sxs-lookup"><span data-stu-id="5b28e-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="5b28e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b28e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b28e-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="5b28e-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="5b28e-108">Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b28e-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="5b28e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b28e-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="5b28e-110">Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="5b28e-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b28e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5b28e-111">Return Value</span></span>

<span data-ttu-id="5b28e-112">Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.</span><span class="sxs-lookup"><span data-stu-id="5b28e-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b28e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b28e-113">Requirements</span></span>



| <span data-ttu-id="5b28e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b28e-114">Requirement</span></span> | <span data-ttu-id="5b28e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5b28e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5b28e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b28e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5b28e-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b28e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5b28e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b28e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5b28e-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5b28e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5b28e-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b28e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b28e-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b28e-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b28e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b28e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b28e-123">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5b28e-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5b28e-124">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5b28e-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





