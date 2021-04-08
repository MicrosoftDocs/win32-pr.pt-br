---
title: Mensagem de ICM_GETSTATE (VFW. h)
description: A \_ mensagem ICM GetState consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- Multimídia do Windows de mensagem ICM_GETSTATE
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086512"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="e3cef-104">\_Mensagem de GETstate do ICM</span><span class="sxs-lookup"><span data-stu-id="e3cef-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="e3cef-105">A mensagem **ICM \_ GetState** consulta um driver de compactação de vídeo para retornar sua configuração atual em um bloco de memória ou para determinar a quantidade de memória necessária para recuperar as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="e3cef-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="e3cef-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="e3cef-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="e3cef-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3cef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3cef-108"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="e3cef-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="e3cef-109">Ponteiro para um bloco de memória para conter as informações de configuração atuais.</span><span class="sxs-lookup"><span data-stu-id="e3cef-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="e3cef-110">Você pode especificar **NULL** para esse parâmetro para determinar a quantidade de memória necessária para as informações de configuração, como em [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span><span class="sxs-lookup"><span data-stu-id="e3cef-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="e3cef-111"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="e3cef-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="e3cef-112">Tamanho, em bytes, do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="e3cef-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3cef-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e3cef-113">Return Value</span></span>

<span data-ttu-id="e3cef-114">Se *VP* for **NULL**, retornará a quantidade de memória, em bytes, necessária para as informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="e3cef-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="e3cef-115">Se *VP* não for **NULL**, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e3cef-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3cef-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3cef-116">Remarks</span></span>

<span data-ttu-id="e3cef-117">A estrutura usada para representar as informações de configuração é específica do driver e é definida pelo driver.</span><span class="sxs-lookup"><span data-stu-id="e3cef-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3cef-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3cef-118">Requirements</span></span>



| <span data-ttu-id="e3cef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cef-119">Requirement</span></span> | <span data-ttu-id="e3cef-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3cef-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3cef-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3cef-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3cef-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e3cef-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3cef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3cef-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3cef-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3cef-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3cef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3cef-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3cef-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3cef-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3cef-128">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e3cef-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e3cef-129">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e3cef-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





