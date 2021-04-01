---
title: Mensagem de ICM_GET (VFW. h)
description: A mensagem de obtenção de ICM \_ recupera um valor DWORD definido pelo aplicativo de um driver de compactação de vídeo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- Multimídia do Windows de mensagem ICM_GET
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644398"
---
# <a name="icm_get-message"></a><span data-ttu-id="58248-104">\_Extrair mensagem do ICM</span><span class="sxs-lookup"><span data-stu-id="58248-104">ICM\_GET message</span></span>

<span data-ttu-id="58248-105">A mensagem de **\_ obtenção de ICM** recupera um valor **DWORD** definido pelo aplicativo de um driver de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="58248-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="58248-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58248-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58248-107"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="58248-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="58248-108">Ponteiro para um bloco de memória a ser preenchido com o estado atual.</span><span class="sxs-lookup"><span data-stu-id="58248-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="58248-109">Você também pode especificar **NULL** para determinar a quantidade de memória exigida pelas informações de estado.</span><span class="sxs-lookup"><span data-stu-id="58248-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="58248-110"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="58248-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="58248-111">Tamanho, em bytes, do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="58248-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58248-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="58248-112">Return Value</span></span>

<span data-ttu-id="58248-113">Retorna a quantidade de memória, em bytes, necessária para armazenar as informações de status.</span><span class="sxs-lookup"><span data-stu-id="58248-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="58248-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="58248-114">Remarks</span></span>

<span data-ttu-id="58248-115">A estrutura usada para representar informações de estado é específica do driver e é definida pelo driver.</span><span class="sxs-lookup"><span data-stu-id="58248-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="58248-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58248-116">Requirements</span></span>



| <span data-ttu-id="58248-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="58248-117">Requirement</span></span> | <span data-ttu-id="58248-118">Valor</span><span class="sxs-lookup"><span data-stu-id="58248-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="58248-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58248-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58248-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58248-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="58248-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58248-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58248-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58248-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="58248-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58248-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58248-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="58248-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58248-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="58248-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58248-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="58248-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="58248-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="58248-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





