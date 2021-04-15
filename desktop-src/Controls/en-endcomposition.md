---
title: EN_ENDCOMPOSITION código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário inseriu novos dados ou terminou de inserir dados ao usar o IME ou a estrutura de serviços de texto.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- EN_ENDCOMPOSITION de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454704"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="b31d8-104">\_Código de notificação de ENDcomposição</span><span class="sxs-lookup"><span data-stu-id="b31d8-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="b31d8-105">Notifica uma janela pai do controle de edição rico que o usuário inseriu novos dados ou terminou de inserir dados ao usar o IME ou a [estrutura de serviços de texto](/windows/desktop/TSF/text-services-framework).</span><span class="sxs-lookup"><span data-stu-id="b31d8-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="b31d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b31d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b31d8-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b31d8-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b31d8-108">Uma estrutura [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) que recebe informações sobre a condição de composição final.</span><span class="sxs-lookup"><span data-stu-id="b31d8-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b31d8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b31d8-109">Requirements</span></span>



| <span data-ttu-id="b31d8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b31d8-110">Requirement</span></span> | <span data-ttu-id="b31d8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b31d8-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b31d8-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b31d8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="b31d8-113">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b31d8-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b31d8-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b31d8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="b31d8-115">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b31d8-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b31d8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b31d8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="b31d8-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b31d8-117"><dt>Richedit.h</dt></span></span> </dl> |



 

