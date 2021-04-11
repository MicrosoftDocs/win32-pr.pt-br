---
description: Notifica um aplicativo quando o IME selecionado precisa da cadeia de caracteres convertida do aplicativo. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros definidos, conforme mostrado abaixo.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4fe46f95b7ad17ba7bb7850ec3fb9ca980519f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169410"
---
# <a name="imr_documentfeed-notification-code"></a><span data-ttu-id="47c33-104">Código de notificação do IMR \_ DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="47c33-104">IMR\_DOCUMENTFEED notification code</span></span>

<span data-ttu-id="47c33-105">Notifica um aplicativo quando o IME selecionado precisa da cadeia de caracteres convertida do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="47c33-105">Notifies an application when the selected IME needs the converted string from the application.</span></span> <span data-ttu-id="47c33-106">O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros definidos, conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="47c33-106">The application receives this command through the [**WM\_IME\_REQUEST**](wm-ime-request.md) message with parameters set as shown below.</span></span>


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a><span data-ttu-id="47c33-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47c33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c33-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="47c33-108"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="47c33-109">Defina como IMR \_ DOCUMENTFEED.</span><span class="sxs-lookup"><span data-stu-id="47c33-109">Set to IMR\_DOCUMENTFEED.</span></span>

</dd> <dt>

<span data-ttu-id="47c33-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="47c33-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="47c33-111">O ponteiro para um buffer que contém a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) .</span><span class="sxs-lookup"><span data-stu-id="47c33-111">Pointer to a buffer to contain the [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c33-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="47c33-112">Return Value</span></span>

<span data-ttu-id="47c33-113">Retorna a estrutura da cadeia de caracteres de reconversão atual.</span><span class="sxs-lookup"><span data-stu-id="47c33-113">Returns the current reconversion string structure.</span></span> <span data-ttu-id="47c33-114">Se *lParam* for definido como **NULL**, o aplicativo retornará o tamanho necessário para que o buffer mantenha a estrutura.</span><span class="sxs-lookup"><span data-stu-id="47c33-114">If *lParam* is set to **NULL**, the application returns the required size for the buffer to hold the structure.</span></span> <span data-ttu-id="47c33-115">O comando retornará 0 se não tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="47c33-115">The command returns 0 if it does not succeed.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c33-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c33-116">Remarks</span></span>

<span data-ttu-id="47c33-117">O IME armazena em cache as cadeias de caracteres convertidas para maior precisão de conversão.</span><span class="sxs-lookup"><span data-stu-id="47c33-117">The IME caches converted strings for higher conversion accuracy.</span></span> <span data-ttu-id="47c33-118">Uma limitação de cache do IME é que ele perde a cadeia de caracteres convertida nas seguintes circunstâncias:</span><span class="sxs-lookup"><span data-stu-id="47c33-118">One caching limitation of the IME is that it loses the converted string under the following circumstances:</span></span>

-   <span data-ttu-id="47c33-119">A posição do cursor para o aplicativo é movida por uma chave, por exemplo, uma tecla de cursor.</span><span class="sxs-lookup"><span data-stu-id="47c33-119">The caret position for the application is moved by a key, for example, a cursor key.</span></span>
-   <span data-ttu-id="47c33-120">A posição do cursor para o aplicativo é movida pelo mouse.</span><span class="sxs-lookup"><span data-stu-id="47c33-120">The caret position for the application is moved by the mouse.</span></span>
-   <span data-ttu-id="47c33-121">Um novo documento é aberto.</span><span class="sxs-lookup"><span data-stu-id="47c33-121">A new document is opened.</span></span>

<span data-ttu-id="47c33-122">Com o comando **IMR \_ DOCUMENTFEED** , o IME pode atualizar suas cadeias de caracteres em cache a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="47c33-122">With the **IMR\_DOCUMENTFEED** command, the IME can refresh its cached strings any time.</span></span> <span data-ttu-id="47c33-123">O uso desse comando melhora a precisão da conversão.</span><span class="sxs-lookup"><span data-stu-id="47c33-123">Use of this command improves conversion accuracy.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c33-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c33-124">Requirements</span></span>



| <span data-ttu-id="47c33-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c33-125">Requirement</span></span> | <span data-ttu-id="47c33-126">Valor</span><span class="sxs-lookup"><span data-stu-id="47c33-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c33-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c33-127">Minimum supported client</span></span><br/> | <span data-ttu-id="47c33-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47c33-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47c33-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c33-129">Minimum supported server</span></span><br/> | <span data-ttu-id="47c33-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47c33-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="47c33-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="47c33-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c33-132"><dt>IMM. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47c33-132"><dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c33-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="47c33-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c33-134">Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="47c33-134">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="47c33-135">Comandos do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="47c33-135">Input Method Manager Commands</span></span>](input-method-manager-commands.md)
</dt> <dt>

[<span data-ttu-id="47c33-136">**Reconverterstring**</span><span class="sxs-lookup"><span data-stu-id="47c33-136">**RECONVERTSTRING**</span></span>](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[<span data-ttu-id="47c33-137">**\_solicitação do IME do WM \_**</span><span class="sxs-lookup"><span data-stu-id="47c33-137">**WM\_IME\_REQUEST**</span></span>](wm-ime-request.md)
</dt> </dl>

 

 




