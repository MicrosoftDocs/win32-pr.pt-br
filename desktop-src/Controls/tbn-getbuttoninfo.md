---
title: TBN_GETBUTTONINFO código de notificação (commctrl. h)
description: Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas sobre quaisquer alterações feitas na barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918854"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="41bff-105">Código de notificação do TBN \_ GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="41bff-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="41bff-106">Recupera informações de personalização da barra de ferramentas e notifica a janela pai da barra de ferramentas sobre quaisquer alterações feitas na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="41bff-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="41bff-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="41bff-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="41bff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41bff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41bff-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41bff-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41bff-110">Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="41bff-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="41bff-111">O membro **iItem** especifica um índice de base zero que fornece uma contagem dos botões que a caixa de diálogo Personalizar barra de ferramentas exibe como ambos disponíveis e presentes na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="41bff-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="41bff-112">O membro **pszText** especifica o endereço do texto do botão atual e **cchText** especifica seu comprimento em caracteres.</span><span class="sxs-lookup"><span data-stu-id="41bff-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="41bff-113">O aplicativo deve preencher a estrutura com informações sobre o botão.</span><span class="sxs-lookup"><span data-stu-id="41bff-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41bff-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41bff-114">Return value</span></span>

<span data-ttu-id="41bff-115">Retorna **true** se as informações do botão foram copiadas para a estrutura especificada; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="41bff-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="41bff-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="41bff-116">Remarks</span></span>

<span data-ttu-id="41bff-117">O controle Toolbar aloca um buffer e o receptor (janela pai) deve copiar o texto para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="41bff-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="41bff-118">O membro **cchText** contém o comprimento do buffer alocado pela barra de ferramentas quando tbn \_ GETBUTTONINFO é enviado para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="41bff-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="41bff-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41bff-119">Requirements</span></span>



| <span data-ttu-id="41bff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="41bff-120">Requirement</span></span> | <span data-ttu-id="41bff-121">Valor</span><span class="sxs-lookup"><span data-stu-id="41bff-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41bff-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41bff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="41bff-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41bff-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41bff-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41bff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="41bff-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41bff-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41bff-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41bff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="41bff-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41bff-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="41bff-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="41bff-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41bff-129">**Tbn \_ GETBUTTONINFOW** (Unicode) e **tbn \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41bff-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





