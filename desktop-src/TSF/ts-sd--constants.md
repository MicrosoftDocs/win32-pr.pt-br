---
title: Constantes de TS_SD_ (Textstor. h)
description: As \_ constantes TS SD \_ \ descrevem os Estados de documento dinâmico usados por um aplicativo em tempo de execução.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761365"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="e08c8-103">Constantes de TS \_ SD \_ \*</span><span class="sxs-lookup"><span data-stu-id="e08c8-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="e08c8-104">As \_ constantes TS SD \_ \* descrevem os Estados de documento dinâmico usados por um aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="e08c8-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="e08c8-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="e08c8-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="e08c8-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e08c8-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="e08c8-107"><dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e08c8-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="e08c8-108">O documento é somente leitura e não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="e08c8-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="e08c8-109"><dt>**TS \_ \_Carregamento de SD**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="e08c8-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="e08c8-110">O documento está sendo carregado e pode estar incompleto.</span><span class="sxs-lookup"><span data-stu-id="e08c8-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="e08c8-111"><dt>**TS \_ SD \_ MASKALL**</dt> <dt>(TS \_ SD \_ ReadOnly de \| TS \_ SD \_ carregando)</dt></span><span class="sxs-lookup"><span data-stu-id="e08c8-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="e08c8-112">O documento é somente leitura e está sendo carregado.</span><span class="sxs-lookup"><span data-stu-id="e08c8-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="e08c8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e08c8-113">Remarks</span></span>

<span data-ttu-id="e08c8-114">O membro **dwDynamicFlags** da estrutura [de \_ status TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) usa essas constantes.</span><span class="sxs-lookup"><span data-stu-id="e08c8-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="e08c8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08c8-115">Requirements</span></span>



| <span data-ttu-id="e08c8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08c8-116">Requirement</span></span> | <span data-ttu-id="e08c8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e08c8-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e08c8-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e08c8-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e08c8-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e08c8-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e08c8-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e08c8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e08c8-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e08c8-122">Redistributable</span></span><br/>          | <span data-ttu-id="e08c8-123">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e08c8-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="e08c8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e08c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08c8-125"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08c8-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="e08c8-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="e08c8-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e08c8-127"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e08c8-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08c8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e08c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08c8-129">STATUS de TS \_</span><span class="sxs-lookup"><span data-stu-id="e08c8-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="e08c8-130">TF \_ as \_ \* constantes do SD</span><span class="sxs-lookup"><span data-stu-id="e08c8-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





