---
title: Mensagem de MCIWNDM_GETPOSITION (VFW. h)
description: A \_ mensagem GETPOSITION MCIWNDM recupera o valor numérico da posição atual dentro do conteúdo do dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETPOSITION
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824218"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="6d939-104">\_Mensagem GETPOSITION MCIWNDM</span><span class="sxs-lookup"><span data-stu-id="6d939-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="6d939-105">A **mensagem \_ GetPosition MCIWNDM** recupera o valor numérico da posição atual dentro do conteúdo do dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="6d939-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="6d939-106">Essa macro também fornece a posição atual no formulário de cadeia de caracteres em um buffer definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6d939-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="6d939-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="6d939-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="6d939-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d939-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d939-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="6d939-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="6d939-110">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="6d939-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="6d939-111">Se a cadeia de caracteres terminada em nulo for maior que o buffer, ela será truncada.</span><span class="sxs-lookup"><span data-stu-id="6d939-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="6d939-112">Use zero para inibir a recuperação da posição como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d939-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="6d939-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="6d939-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="6d939-114">Ponteiro para um buffer definido pelo aplicativo usado para retornar a posição.</span><span class="sxs-lookup"><span data-stu-id="6d939-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="6d939-115">Use zero para inibir a recuperação da posição como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6d939-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="6d939-116">Se o dispositivo oferecer suporte a faixas, as informações de posição da cadeia de caracteres serão retornadas no formato TT: MM: SS: FF, em que TT corresponde a faixas, MM e SS correspondem a minutos e segundos, e FF corresponde a quadros.</span><span class="sxs-lookup"><span data-stu-id="6d939-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d939-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6d939-117">Return Value</span></span>

<span data-ttu-id="6d939-118">Retorna um inteiro correspondente à posição atual.</span><span class="sxs-lookup"><span data-stu-id="6d939-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="6d939-119">As unidades para o valor de posição dependem do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="6d939-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d939-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d939-120">Requirements</span></span>



| <span data-ttu-id="6d939-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d939-121">Requirement</span></span> | <span data-ttu-id="6d939-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6d939-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d939-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d939-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d939-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d939-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6d939-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d939-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d939-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d939-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6d939-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d939-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d939-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d939-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d939-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d939-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d939-130">**MCIWndGetPosition**</span><span class="sxs-lookup"><span data-stu-id="6d939-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="6d939-131">**MCIWndGetPositionString**</span><span class="sxs-lookup"><span data-stu-id="6d939-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





