---
title: Função de retorno de chamada ICMProgressProcCallback
description: A função ICMProgressProcCallback é uma função de retorno de chamada fornecida pelo aplicativo que relata o progresso e permite que o aplicativo cancele o processamento de cores.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Função de retorno de chamada ICMProgressProcCallback sistema de cores do Windows
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769668"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="4c26f-104">Função de retorno de chamada ICMProgressProcCallback</span><span class="sxs-lookup"><span data-stu-id="4c26f-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="4c26f-105">A função **ICMProgressProcCallback** é uma função de retorno de chamada fornecida pelo aplicativo que relata o progresso e permite que o aplicativo cancele o processamento de cores.</span><span class="sxs-lookup"><span data-stu-id="4c26f-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c26f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c26f-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="4c26f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c26f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c26f-108">*ulMax*</span><span class="sxs-lookup"><span data-stu-id="4c26f-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="4c26f-109">Especifica o valor máximo do contador de progresso (usado para estimar a conclusão do processamento de bitmap).</span><span class="sxs-lookup"><span data-stu-id="4c26f-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="4c26f-110">*ulCurrent*</span><span class="sxs-lookup"><span data-stu-id="4c26f-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="4c26f-111">Especifica o valor atual do contador de progresso (quando dividido pelo valor máximo, fornece uma estimativa aproximada da porcentagem de conclusão).</span><span class="sxs-lookup"><span data-stu-id="4c26f-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="4c26f-112">*ulCallbackData*</span><span class="sxs-lookup"><span data-stu-id="4c26f-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="4c26f-113">Especifica os dados que são passados pelo aplicativo para uma função ICM2, que então o passa para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4c26f-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="4c26f-114">Esses dados podem ser usados, por exemplo, para identificar o bitmap e o processo sobre o qual o progresso está sendo relatado.</span><span class="sxs-lookup"><span data-stu-id="4c26f-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c26f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c26f-115">Return value</span></span>

<span data-ttu-id="4c26f-116">Essa função retorna **true** para continuar o processamento de bitmap.</span><span class="sxs-lookup"><span data-stu-id="4c26f-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="4c26f-117">O valor de retorno é **false** para cancelar o processamento.</span><span class="sxs-lookup"><span data-stu-id="4c26f-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="4c26f-118">Se o processamento for cancelado, a função de chamada retornará zero para indicar falha, embora seu buffer de saída possa ser parcialmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="4c26f-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c26f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c26f-119">Remarks</span></span>

<span data-ttu-id="4c26f-120">O nome dessa função de retorno de chamada é fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c26f-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="4c26f-121">Várias funções WCS, incluindo [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) e [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), chamam essa função periodicamente.</span><span class="sxs-lookup"><span data-stu-id="4c26f-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c26f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c26f-122">Requirements</span></span>



| <span data-ttu-id="4c26f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c26f-123">Requirement</span></span> | <span data-ttu-id="4c26f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4c26f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c26f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c26f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4c26f-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c26f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4c26f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c26f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4c26f-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c26f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4c26f-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c26f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c26f-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c26f-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c26f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c26f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c26f-132">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="4c26f-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="4c26f-133">Funções</span><span class="sxs-lookup"><span data-stu-id="4c26f-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="4c26f-134">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="4c26f-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="4c26f-135">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="4c26f-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
