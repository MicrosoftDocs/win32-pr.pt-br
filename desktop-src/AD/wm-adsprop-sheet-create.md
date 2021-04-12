---
title: WM_ADSPROP_SHEET_CREATE mensagem
description: Enviado ao objeto de notificação para criar uma folha de propriedades secundária em um Active Directory snap-in do MMC.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499394"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="409d4-104">\_ \_ Página \_ criar mensagem do WM ADSPROP</span><span class="sxs-lookup"><span data-stu-id="409d4-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="409d4-105">A mensagem de **\_ criação da \_ planilha \_ do WM ADSPROP** é enviada ao objeto de notificação para criar uma folha de propriedades secundária em um snap-in do Active Directory MMC.</span><span class="sxs-lookup"><span data-stu-id="409d4-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="409d4-106">Esse valor de mensagem não está definido em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="409d4-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="409d4-107">Para usar esse valor de mensagem, você mesmo deve defini-lo no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="409d4-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="409d4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="409d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="409d4-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="409d4-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="409d4-110">O identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="409d4-110">The handle of the notification object.</span></span> <span data-ttu-id="409d4-111">Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="409d4-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="409d4-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="409d4-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="409d4-113">Contém um ponteiro para uma estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) que define a página secundária a ser criada.</span><span class="sxs-lookup"><span data-stu-id="409d4-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="409d4-114">Somente uma folha de propriedades secundária pode ser criada com **a \_ planilha do WM ADSPROP \_ \_ criar** mensagem para que a estrutura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) possa conter apenas uma estrutura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="409d4-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="409d4-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="409d4-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="409d4-116">Não usado.</span><span class="sxs-lookup"><span data-stu-id="409d4-116">Not used.</span></span> <span data-ttu-id="409d4-117">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="409d4-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="409d4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="409d4-118">Return value</span></span>

<span data-ttu-id="409d4-119">O valor de retorno para essa mensagem é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="409d4-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="409d4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="409d4-120">Remarks</span></span>

<span data-ttu-id="409d4-121">O chamador deve alocar a estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) , a cadeia de título e todas as cadeias de caracteres [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) usando uma única chamada para a função [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) .</span><span class="sxs-lookup"><span data-stu-id="409d4-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="409d4-122">A mensagem de **\_ criação da \_ planilha \_ do WM ADSPROP** é uma mensagem assíncrona, portanto, será retornada antes da criação da planilha secundária.</span><span class="sxs-lookup"><span data-stu-id="409d4-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="409d4-123">Por isso, a memória deve permanecer intacta após o retorno da mensagem.</span><span class="sxs-lookup"><span data-stu-id="409d4-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="409d4-124">O receptor liberará essa memória com uma única chamada para a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) depois que a planilha secundária for criada.</span><span class="sxs-lookup"><span data-stu-id="409d4-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="409d4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="409d4-125">Requirements</span></span>



| <span data-ttu-id="409d4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="409d4-126">Requirement</span></span> | <span data-ttu-id="409d4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="409d4-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="409d4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="409d4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="409d4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="409d4-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="409d4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="409d4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="409d4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="409d4-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="409d4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="409d4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="409d4-133">**CFSTR \_ DS \_ PARENTHWND**</span><span class="sxs-lookup"><span data-stu-id="409d4-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="409d4-134">**\_ \_ informações da página DSA SEC \_**</span><span class="sxs-lookup"><span data-stu-id="409d4-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="409d4-135">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="409d4-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="409d4-136">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="409d4-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="409d4-137">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="409d4-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="409d4-138">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="409d4-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

