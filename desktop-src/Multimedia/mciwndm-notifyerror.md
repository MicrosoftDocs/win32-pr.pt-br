---
title: Mensagem de MCIWNDM_NOTIFYERROR (VFW. h)
description: A \_ mensagem MCIWNDM NOTIFYERROR notifica a janela pai de um aplicativo de que ocorreu um erro MCI.
ms.assetid: 0f54886a-77dc-43cc-be46-2d322c75471a
keywords:
- Multimídia do Windows de mensagem MCIWNDM_NOTIFYERROR
topic_type:
- apiref
api_name:
- MCIWNDM_NOTIFYERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbef9180c31091f3bd1a85f23a08990c2f7e7ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009239"
---
# <a name="mciwndm_notifyerror-message"></a><span data-ttu-id="e5557-104">\_Mensagem MCIWNDM NOTIFYERROR</span><span class="sxs-lookup"><span data-stu-id="e5557-104">MCIWNDM\_NOTIFYERROR message</span></span>

<span data-ttu-id="e5557-105">A mensagem **MCIWNDM \_ NOTIFYERROR** notifica a janela pai de um aplicativo de que ocorreu um erro MCI.</span><span class="sxs-lookup"><span data-stu-id="e5557-105">The **MCIWNDM\_NOTIFYERROR** message notifies the parent window of an application that an MCI error occurred.</span></span>


```C++
MCIWNDM_NOTIFYERROR 
wParam = (WPARAM) (HWND) hwnd; 
lParam = (LPARAM) (LONG) errorCode; 
```



## <a name="parameters"></a><span data-ttu-id="e5557-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5557-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5557-107"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="e5557-107"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="e5557-108">Manipule a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="e5557-108">Handle to the MCIWnd window.</span></span>

</dd> <dt>

<span data-ttu-id="e5557-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span><span class="sxs-lookup"><span data-stu-id="e5557-109"><span id="errorCode"></span><span id="errorcode"></span><span id="ERRORCODE"></span>*errorCode*</span></span>
</dt> <dd>

<span data-ttu-id="e5557-110">Código numérico para o erro MCI.</span><span class="sxs-lookup"><span data-stu-id="e5557-110">Numerical code for the MCI error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5557-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5557-111">Remarks</span></span>

<span data-ttu-id="e5557-112">Você pode habilitar a notificação de erro MCI especificando o \_ estilo de janela MCIWNDF NOTIFYERROR.</span><span class="sxs-lookup"><span data-stu-id="e5557-112">You can enable MCI error notification by specifying the MCIWNDF\_NOTIFYERROR window style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5557-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5557-113">Requirements</span></span>



| <span data-ttu-id="e5557-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5557-114">Requirement</span></span> | <span data-ttu-id="e5557-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e5557-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5557-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5557-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e5557-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5557-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e5557-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5557-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e5557-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5557-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5557-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5557-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5557-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5557-121"><dt>Vfw.h</dt></span></span> </dl> |



 

 





