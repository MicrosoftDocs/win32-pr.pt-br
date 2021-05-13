---
description: Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou termina o assistente se não houver mais páginas do lado do cliente.
title: Método WebWizardHost.FinalNext (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841837"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="dfaf4-103">Método WebWizardHost.FinalNext</span><span class="sxs-lookup"><span data-stu-id="dfaf4-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="dfaf4-104">Navega até a página do assistente do lado do cliente que segue a página que hospeda as páginas HTML do lado do servidor ou termina o assistente se não houver mais páginas do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="dfaf4-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfaf4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfaf4-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="dfaf4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfaf4-106">Parameters</span></span>

<span data-ttu-id="dfaf4-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dfaf4-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfaf4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfaf4-108">Remarks</span></span>

<span data-ttu-id="dfaf4-109">Quando o assistente estiver exibindo a última página HTML  do  lado do servidor e o usuário clicar no botão Próximo ou Concluir, o servidor invocará **FinalNext** no manipulador de eventos desse botão.</span><span class="sxs-lookup"><span data-stu-id="dfaf4-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfaf4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfaf4-110">Requirements</span></span>



| <span data-ttu-id="dfaf4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfaf4-111">Requirement</span></span> | <span data-ttu-id="dfaf4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="dfaf4-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaf4-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaf4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dfaf4-114">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dfaf4-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dfaf4-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfaf4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dfaf4-116">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfaf4-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dfaf4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfaf4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfaf4-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dfaf4-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfaf4-119">Idl</span><span class="sxs-lookup"><span data-stu-id="dfaf4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfaf4-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfaf4-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




