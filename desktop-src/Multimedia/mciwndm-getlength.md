---
title: Mensagem de MCIWNDM_GETLENGTH (VFW. h)
description: A \_ mensagem MCIWNDM GETLENGTH recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETLENGTH
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454750"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="ab415-105">\_Mensagem MCIWNDM GETLENGTH</span><span class="sxs-lookup"><span data-stu-id="ab415-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="ab415-106">A mensagem **MCIWNDM \_ GETLENGTH** recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="ab415-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="ab415-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="ab415-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ab415-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ab415-108">Return Value</span></span>

<span data-ttu-id="ab415-109">Retorna o comprimento.</span><span class="sxs-lookup"><span data-stu-id="ab415-109">Returns the length.</span></span> <span data-ttu-id="ab415-110">As unidades para o comprimento dependem do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="ab415-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab415-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab415-111">Requirements</span></span>



| <span data-ttu-id="ab415-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab415-112">Requirement</span></span> | <span data-ttu-id="ab415-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ab415-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ab415-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab415-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ab415-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab415-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ab415-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab415-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ab415-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab415-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ab415-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab415-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab415-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab415-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab415-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab415-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab415-121">**MCIWndGetLength**</span><span class="sxs-lookup"><span data-stu-id="ab415-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





