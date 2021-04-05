---
title: Mensagem de WM_ADSPROP_NOTIFY_ERROR (Adsprop. h)
description: A mensagem de erro de notificação do WM \_ ADSPROP \_ \_ adiciona uma mensagem de erro a uma lista de mensagens de erro que são exibidas chamando a função ADsPropShowErrorDialog.
ms.assetid: 7abf1b3d-5abe-42cd-baeb-1bf863c7f04d
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_ERROR Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_ERROR
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9cdcb33c5536cfa67ab136daa5aa56d93f1d706
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085593"
---
# <a name="wm_adsprop_notify_error-message"></a><span data-ttu-id="33859-104">\_Mensagem de \_ erro de notificação do WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="33859-104">WM\_ADSPROP\_NOTIFY\_ERROR message</span></span>

<span data-ttu-id="33859-105">A mensagem de **erro de notificação do WM \_ \_ \_ ADSPROP** adiciona uma mensagem de erro a uma lista de mensagens de erro que são exibidas chamando a função [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) .</span><span class="sxs-lookup"><span data-stu-id="33859-105">The **WM\_ADSPROP\_NOTIFY\_ERROR** message adds an error message to a list of error messages that are displayed by calling the [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) function.</span></span>


```C++
WM_ADSPROP_NOTIFY_ERROR

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="33859-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33859-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="33859-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="33859-108">Identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="33859-108">Handle of the notification object.</span></span> <span data-ttu-id="33859-109">Esse é o parâmetro *hNotifyObject* obtido por [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="33859-109">This is the *hNotifyObject* parameter obtained by [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="33859-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33859-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33859-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="33859-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="33859-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33859-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33859-113">Ponteiro para uma estrutura [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) que contém dados de mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="33859-113">Pointer to an [**ADSPROPERROR**](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror) structure that contains error message data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33859-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33859-114">Return value</span></span>

<span data-ttu-id="33859-115">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="33859-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33859-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="33859-116">Remarks</span></span>

<span data-ttu-id="33859-117">A função [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) é o método preferencial para enviar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="33859-117">The [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) function is the preferred method of sending this message.</span></span>

<span data-ttu-id="33859-118">As mensagens de erro adicionadas pela mensagem de **erro de notificação do WM \_ \_ \_ ADSPROP** são acumuladas até que [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="33859-118">The error messages added by the **WM\_ADSPROP\_NOTIFY\_ERROR** message are accumulated until [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) is called.</span></span> <span data-ttu-id="33859-119">**ADsPropShowErrorDialog** combina e exibe as mensagens de erro acumuladas.</span><span class="sxs-lookup"><span data-stu-id="33859-119">**ADsPropShowErrorDialog** combines and displays the accumulated error messages.</span></span> <span data-ttu-id="33859-120">Quando a caixa de diálogo de erro é ignorada, as mensagens de erro acumuladas são excluídas.</span><span class="sxs-lookup"><span data-stu-id="33859-120">When the error dialog is dismissed, the accumulated error messages are deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="33859-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33859-121">Requirements</span></span>



| <span data-ttu-id="33859-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="33859-122">Requirement</span></span> | <span data-ttu-id="33859-123">Valor</span><span class="sxs-lookup"><span data-stu-id="33859-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33859-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33859-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33859-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33859-125">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="33859-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33859-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33859-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33859-127">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="33859-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33859-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="33859-129"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="33859-129"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33859-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="33859-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33859-131">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="33859-131">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="33859-132">**ADSPROPERROR**</span><span class="sxs-lookup"><span data-stu-id="33859-132">**ADSPROPERROR**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adsproperror)
</dt> <dt>

[<span data-ttu-id="33859-133">**ADsPropSendErrorMessage**</span><span class="sxs-lookup"><span data-stu-id="33859-133">**ADsPropSendErrorMessage**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage)
</dt> <dt>

[<span data-ttu-id="33859-134">**ADsPropShowErrorDialog**</span><span class="sxs-lookup"><span data-stu-id="33859-134">**ADsPropShowErrorDialog**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog)
</dt> </dl>

 

 





