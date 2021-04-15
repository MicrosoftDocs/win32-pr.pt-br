---
title: Mensagem de MCIWNDM_GETDEVICE (VFW. h)
description: A \_ mensagem GETdevice do MCIWNDM recupera o nome do dispositivo MCI aberto no momento. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDevice.
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETDEVICE
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454752"
---
# <a name="mciwndm_getdevice-message"></a><span data-ttu-id="66fd3-105">Mensagem do MCIWNDM \_ GETdevice</span><span class="sxs-lookup"><span data-stu-id="66fd3-105">MCIWNDM\_GETDEVICE message</span></span>

<span data-ttu-id="66fd3-106">A **mensagem \_ GetDevice do MCIWNDM** recupera o nome do dispositivo MCI aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="66fd3-106">The **MCIWNDM\_GETDEVICE** message retrieves the name of the currently open MCI device.</span></span> <span data-ttu-id="66fd3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="66fd3-107">You can send this message explicitly or by using the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span>


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="66fd3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66fd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66fd3-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="66fd3-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="66fd3-110">Tamanho, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="66fd3-110">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="66fd3-111"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="66fd3-111"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="66fd3-112">Ponteiro para um buffer definido pelo aplicativo para retornar o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66fd3-112">Pointer to an application-defined buffer to return the device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66fd3-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="66fd3-113">Return Value</span></span>

<span data-ttu-id="66fd3-114">Retornará zero se for bem-sucedido ou um valor diferente de zero, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="66fd3-114">Returns zero if successful or a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66fd3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="66fd3-115">Remarks</span></span>

<span data-ttu-id="66fd3-116">Se a cadeia de caracteres terminada em nulo que contém o nome do dispositivo for maior do que o buffer, MCIWnd o truncará.</span><span class="sxs-lookup"><span data-stu-id="66fd3-116">If the null-terminated string containing the device name is longer than the buffer, MCIWnd truncates it.</span></span>

## <a name="requirements"></a><span data-ttu-id="66fd3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66fd3-117">Requirements</span></span>



| <span data-ttu-id="66fd3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="66fd3-118">Requirement</span></span> | <span data-ttu-id="66fd3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="66fd3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="66fd3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66fd3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66fd3-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66fd3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66fd3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66fd3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66fd3-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66fd3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66fd3-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="66fd3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66fd3-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fd3-125"><dt>Vfw.h</dt></span></span> </dl> |



 

 





