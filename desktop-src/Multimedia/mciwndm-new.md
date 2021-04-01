---
title: Mensagem de MCIWNDM_NEW (VFW. h)
description: A \_ nova mensagem do MCIWNDM cria um novo arquivo para o dispositivo MCI atual. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NEW
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644565"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="9a7f4-105">MCIWNDM \_ nova mensagem</span><span class="sxs-lookup"><span data-stu-id="9a7f4-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="9a7f4-106">A **\_ nova** mensagem do MCIWNDM cria um novo arquivo para o dispositivo MCI atual.</span><span class="sxs-lookup"><span data-stu-id="9a7f4-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="9a7f4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .</span><span class="sxs-lookup"><span data-stu-id="9a7f4-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="9a7f4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a7f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7f4-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="9a7f4-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="9a7f4-110">Ponteiro para um buffer que contém o nome do dispositivo MCI que usará o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a7f4-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7f4-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9a7f4-111">Return Value</span></span>

<span data-ttu-id="9a7f4-112">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9a7f4-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7f4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7f4-113">Requirements</span></span>



| <span data-ttu-id="9a7f4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7f4-114">Requirement</span></span> | <span data-ttu-id="9a7f4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9a7f4-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9a7f4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a7f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7f4-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a7f4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="9a7f4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a7f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7f4-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9a7f4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9a7f4-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9a7f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7f4-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f4-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7f4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a7f4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7f4-123">**MCIWndNew**</span><span class="sxs-lookup"><span data-stu-id="9a7f4-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





