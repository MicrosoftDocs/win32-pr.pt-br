---
title: Mensagem de ICM_SETSTATE (VFW. h)
description: A \_ mensagem ICM SetState notifica um driver de compactação de vídeo para definir o estado do compressor. Você pode enviar essa mensagem explicitamente ou usando a macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- Multimídia do Windows de mensagem ICM_SETSTATE
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779617"
---
# <a name="icm_setstate-message"></a><span data-ttu-id="ee2f3-105">\_Mensagem SETstate do ICM</span><span class="sxs-lookup"><span data-stu-id="ee2f3-105">ICM\_SETSTATE message</span></span>

<span data-ttu-id="ee2f3-106">A mensagem **ICM \_ SetState** notifica um driver de compactação de vídeo para definir o estado do compressor.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-106">The **ICM\_SETSTATE** message notifies a video compression driver to set the state of the compressor.</span></span> <span data-ttu-id="ee2f3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="ee2f3-107">You can send this message explicitly or by using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span>


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="ee2f3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee2f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee2f3-109"><span id="pv"></span><span id="PV"></span>*PV*</span><span class="sxs-lookup"><span data-stu-id="ee2f3-109"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="ee2f3-110">Ponteiro para um bloco de memória que contém dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-110">Pointer to a block of memory containing configuration data.</span></span> <span data-ttu-id="ee2f3-111">Você pode especificar **NULL** para esse parâmetro para redefinir o compressor para seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-111">You can specify **NULL** for this parameter to reset the compressor to its default state.</span></span>

</dd> <dt>

<span data-ttu-id="ee2f3-112"><span id="cb"></span><span id="CB"></span>*CB*</span><span class="sxs-lookup"><span data-stu-id="ee2f3-112"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="ee2f3-113">Tamanho, em bytes, do bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-113">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee2f3-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ee2f3-114">Return Value</span></span>

<span data-ttu-id="ee2f3-115">Retorna o número de bytes usados pelo compactador, se for bem-sucedido ou zero.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-115">Returns the number of bytes used by the compressor if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee2f3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee2f3-116">Remarks</span></span>

<span data-ttu-id="ee2f3-117">As informações usadas por essa mensagem são privadas e específicas para um determinado compressor.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-117">The information used by this message is private and specific to a given compressor.</span></span> <span data-ttu-id="ee2f3-118">Os aplicativos cliente devem usar essa mensagem somente para restaurar as informações obtidas anteriormente com a mensagem [**ICM \_ GetState**](icm-getstate.md) e devem usar a mensagem [**ICM \_ Configure**](icm-configure.md) para ajustar a configuração de um driver de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ee2f3-118">Client applications should use this message only to restore information previously obtained with the [**ICM\_GETSTATE**](icm-getstate.md) message and should use the [**ICM\_CONFIGURE**](icm-configure.md) message to adjust the configuration of a video compression driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2f3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2f3-119">Requirements</span></span>



| <span data-ttu-id="ee2f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2f3-120">Requirement</span></span> | <span data-ttu-id="ee2f3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ee2f3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ee2f3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee2f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2f3-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee2f3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ee2f3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee2f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2f3-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ee2f3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ee2f3-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ee2f3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee2f3-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee2f3-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee2f3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee2f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee2f3-129">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ee2f3-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ee2f3-130">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ee2f3-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





