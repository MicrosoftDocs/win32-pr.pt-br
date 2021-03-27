---
description: Solicita o título e o texto de um InfoTip de divisa para o item especificado pela estrutura SMDATA que o acompanha.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Mensagem de SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968056"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="41f84-103">Mensagem do SMC \_ CHEVRONGETTIP</span><span class="sxs-lookup"><span data-stu-id="41f84-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="41f84-104">Solicita o título e o texto de um InfoTip de divisa para o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="41f84-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="41f84-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41f84-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f84-106">*pwszTipTitle*</span><span class="sxs-lookup"><span data-stu-id="41f84-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="41f84-107">Um ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que contém o título de InfoTip.</span><span class="sxs-lookup"><span data-stu-id="41f84-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="41f84-108">Essa cadeia de caracteres não deve ultrapassar o máximo de \_ caracteres de caminho, incluindo o caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="41f84-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="41f84-109">*pwszTipText*</span><span class="sxs-lookup"><span data-stu-id="41f84-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="41f84-110">Um ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que contém o texto de InfoTip.</span><span class="sxs-lookup"><span data-stu-id="41f84-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="41f84-111">Essa cadeia de caracteres não deve ultrapassar o máximo de \_ caracteres de caminho, incluindo o caractere **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="41f84-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f84-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41f84-112">Return value</span></span>

<span data-ttu-id="41f84-113">Retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="41f84-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f84-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="41f84-114">Remarks</span></span>

<span data-ttu-id="41f84-115">Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="41f84-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f84-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f84-116">Requirements</span></span>



| <span data-ttu-id="41f84-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f84-117">Requirement</span></span> | <span data-ttu-id="41f84-118">Valor</span><span class="sxs-lookup"><span data-stu-id="41f84-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41f84-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f84-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41f84-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41f84-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="41f84-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41f84-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41f84-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="41f84-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41f84-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="41f84-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f84-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f84-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="41f84-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="41f84-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41f84-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41f84-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




