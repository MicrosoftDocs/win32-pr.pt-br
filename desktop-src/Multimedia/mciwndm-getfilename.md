---
title: Mensagem de MCIWNDM_GETFILENAME (VFW. h)
description: A \_ mensagem MCIWNDM GETFILENAME recupera o nome de arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetFileName.
ms.assetid: d61b1b6d-0fae-4732-993c-41e08a4e05be
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETFILENAME
topic_type:
- apiref
api_name:
- MCIWNDM_GETFILENAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 232a1d829b5cdd6da23e7dd3fb0294b95ca79f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499257"
---
# <a name="mciwndm_getfilename-message"></a><span data-ttu-id="cb6ef-105">\_Mensagem MCIWNDM GETFILENAME</span><span class="sxs-lookup"><span data-stu-id="cb6ef-105">MCIWNDM\_GETFILENAME message</span></span>

<span data-ttu-id="cb6ef-106">A mensagem **MCIWNDM \_ GETFILENAME** recupera o nome de arquivo usado atualmente por um dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="cb6ef-106">The **MCIWNDM\_GETFILENAME** message retrieves the filename currently used by an MCI device.</span></span> <span data-ttu-id="cb6ef-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="cb6ef-107">You can send this message explicitly or by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span>


```C++
MCIWNDM_GETFILENAME 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="cb6ef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb6ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6ef-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="cb6ef-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="cb6ef-110">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="cb6ef-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cb6ef-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="cb6ef-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="cb6ef-112">Ponteiro para um buffer definido pelo aplicativo para retornar o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cb6ef-112">Pointer to an application-defined buffer to return the filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6ef-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cb6ef-113">Return Value</span></span>

<span data-ttu-id="cb6ef-114">Retornará zero se for bem-sucedido ou 1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cb6ef-114">Returns zero if successful or 1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6ef-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb6ef-115">Remarks</span></span>

<span data-ttu-id="cb6ef-116">Se a cadeia de caracteres terminada em nulo que contém o nome do arquivo for maior do que o buffer, MCIWnd truncará o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cb6ef-116">If the null-terminated string containing the filename is longer than the buffer, MCIWnd truncates the filename.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6ef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb6ef-117">Requirements</span></span>



| <span data-ttu-id="cb6ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6ef-118">Requirement</span></span> | <span data-ttu-id="cb6ef-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cb6ef-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cb6ef-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6ef-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb6ef-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cb6ef-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6ef-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb6ef-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb6ef-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb6ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6ef-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6ef-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb6ef-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb6ef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6ef-127">**MCIWndGetFileName**</span><span class="sxs-lookup"><span data-stu-id="cb6ef-127">**MCIWndGetFileName**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
</dt> </dl>

 

 





