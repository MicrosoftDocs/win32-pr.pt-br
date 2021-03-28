---
description: Define a posição de um item na exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETITEMPOS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171870"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="46030-104">\_Mensagem SFVM SETITEMPOS</span><span class="sxs-lookup"><span data-stu-id="46030-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="46030-105">Define a posição de um item na exibição do Shell.</span><span class="sxs-lookup"><span data-stu-id="46030-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="46030-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="46030-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="46030-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46030-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46030-108">*SIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46030-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46030-109">Um ponteiro para uma estrutura [**SFV \_ SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .</span><span class="sxs-lookup"><span data-stu-id="46030-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46030-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46030-110">Requirements</span></span>



| <span data-ttu-id="46030-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="46030-111">Requirement</span></span> | <span data-ttu-id="46030-112">Valor</span><span class="sxs-lookup"><span data-stu-id="46030-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46030-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46030-113">Minimum supported client</span></span><br/> | <span data-ttu-id="46030-114">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="46030-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46030-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46030-115">Minimum supported server</span></span><br/> | <span data-ttu-id="46030-116">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46030-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46030-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46030-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="46030-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="46030-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




