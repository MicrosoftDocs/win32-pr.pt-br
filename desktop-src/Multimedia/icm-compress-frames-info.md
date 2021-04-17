---
title: Mensagem de ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: A \_ mensagem de informações de quadros de compactação ICM \_ \_ Notifica um driver de compactação para definir os parâmetros para a compactação pendente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_FRAMES_INFO
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455729"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="fce80-104">\_Mensagem de \_ informações de quadros de COMPACTação ICM \_</span><span class="sxs-lookup"><span data-stu-id="fce80-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="fce80-105">A mensagem de **\_ informações de \_ quadros \_ de compactação ICM** notifica um driver de compactação para definir os parâmetros para a compactação pendente.</span><span class="sxs-lookup"><span data-stu-id="fce80-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="fce80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fce80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce80-107"><span id="icf"></span><span id="ICF"></span>*ICF*</span><span class="sxs-lookup"><span data-stu-id="fce80-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="fce80-108">Ponteiro para uma estrutura [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) .</span><span class="sxs-lookup"><span data-stu-id="fce80-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="fce80-109">Os membros **GetData** e **PutData** dessa estrutura não são usados com esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="fce80-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="fce80-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="fce80-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="fce80-111">Tamanho, em bytes, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span><span class="sxs-lookup"><span data-stu-id="fce80-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce80-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fce80-112">Return Value</span></span>

<span data-ttu-id="fce80-113">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="fce80-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce80-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fce80-114">Remarks</span></span>

<span data-ttu-id="fce80-115">Um compressor pode usar essa mensagem para determinar a quantidade de espaço a ser alocada para cada quadro durante a compactação.</span><span class="sxs-lookup"><span data-stu-id="fce80-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce80-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce80-116">Requirements</span></span>



| <span data-ttu-id="fce80-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce80-117">Requirement</span></span> | <span data-ttu-id="fce80-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fce80-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fce80-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fce80-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fce80-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fce80-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fce80-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fce80-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fce80-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fce80-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fce80-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fce80-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fce80-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fce80-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce80-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fce80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce80-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="fce80-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="fce80-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="fce80-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





