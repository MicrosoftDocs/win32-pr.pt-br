---
title: Mensagem de MCIWNDM_PUT_SOURCE (VFW. h)
description: A \_ mensagem de origem MCIWNDM Put \_ define as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- Multimídia do Windows de mensagem MCIWNDM_PUT_SOURCE
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644228"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="63588-105">MCIWNDM \_ colocar \_ mensagem de origem</span><span class="sxs-lookup"><span data-stu-id="63588-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="63588-106">A mensagem de **\_ \_ origem MCIWNDM Put** define as coordenadas do retângulo de origem usado para cortar as imagens de um arquivo AVI durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="63588-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="63588-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .</span><span class="sxs-lookup"><span data-stu-id="63588-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="63588-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63588-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63588-109"><span id="prc"></span><span id="PRC"></span>*popular*</span><span class="sxs-lookup"><span data-stu-id="63588-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="63588-110">Ponteiro para uma estrutura [Rect](/previous-versions//ms536136(v=vs.85)) que contém as coordenadas do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="63588-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63588-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="63588-111">Return Value</span></span>

<span data-ttu-id="63588-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="63588-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="63588-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63588-113">Requirements</span></span>



| <span data-ttu-id="63588-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="63588-114">Requirement</span></span> | <span data-ttu-id="63588-115">Valor</span><span class="sxs-lookup"><span data-stu-id="63588-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="63588-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63588-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63588-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63588-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="63588-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63588-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63588-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="63588-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="63588-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63588-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63588-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="63588-121"><dt>Vfw.h</dt></span></span> </dl> |



 

