---
description: Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.
title: Método WebWizardHost. FinalBack (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828750"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="398f1-103">Método WebWizardHost. FinalBack</span><span class="sxs-lookup"><span data-stu-id="398f1-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="398f1-104">Navega até a página do lado do cliente imediatamente antes da página que hospeda as páginas HTML do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="398f1-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="398f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="398f1-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="398f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="398f1-106">Parameters</span></span>

<span data-ttu-id="398f1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="398f1-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="398f1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="398f1-108">Remarks</span></span>

<span data-ttu-id="398f1-109">Quando o assistente exibe a primeira página do lado do servidor e o usuário clica no botão **voltar** , o servidor invoca **FinalBack** quando notificado sobre esse evento pelo manipulador de eventos do cliente.</span><span class="sxs-lookup"><span data-stu-id="398f1-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="398f1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="398f1-110">Requirements</span></span>



| <span data-ttu-id="398f1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="398f1-111">Requirement</span></span> | <span data-ttu-id="398f1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="398f1-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="398f1-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398f1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="398f1-114">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="398f1-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="398f1-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398f1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="398f1-116">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="398f1-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="398f1-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="398f1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="398f1-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="398f1-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="398f1-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="398f1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="398f1-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="398f1-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




