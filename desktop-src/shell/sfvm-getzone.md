---
description: 'Permite que o objeto de retorno de chamada forneça informações de zona da Internet. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Mensagem de SFVM_GETZONE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506237"
---
# <a name="sfvm_getzone-message"></a><span data-ttu-id="8c68b-104">SFVM \_ mensagem GETzone</span><span class="sxs-lookup"><span data-stu-id="8c68b-104">SFVM\_GETZONE message</span></span>

<span data-ttu-id="8c68b-105">\[Essa notificação é suportada por meio do Windows XP Service Pack 2 (SP2) e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8c68b-105">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="8c68b-106">Ele pode não ter suporte em versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c68b-106">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8c68b-107">Permite que o objeto de retorno de chamada forneça informações de zona da Internet.</span><span class="sxs-lookup"><span data-stu-id="8c68b-107">Allows the callback object to provide Internet zone information.</span></span> <span data-ttu-id="8c68b-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8c68b-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a><span data-ttu-id="8c68b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c68b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c68b-110">*zona* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8c68b-110">*zone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c68b-111">Um dos valores a seguir indicando a zona da Internet.</span><span class="sxs-lookup"><span data-stu-id="8c68b-111">One of the following values indicating the Internet zone.</span></span> <span data-ttu-id="8c68b-112">Esses valores constituem a enumeração [**UrlZone**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , definida em Urlmon. h.</span><span class="sxs-lookup"><span data-stu-id="8c68b-112">These values constitute the [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) enumeration, defined in Urlmon.h.</span></span>

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span data-ttu-id="8c68b-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_computador local \_ UrlZone**</span><span class="sxs-lookup"><span data-stu-id="8c68b-113"><span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**URLZONE\_LOCAL\_MACHINE**</span></span>


</dt> <dd>

<span data-ttu-id="8c68b-114">Zona usada para conteúdo que já está no computador local do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c68b-114">Zone used for content already on the user's local computer.</span></span> <span data-ttu-id="8c68b-115">Essa zona não é exposta pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c68b-115">This zone is not exposed by the user interface.</span></span>

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span data-ttu-id="8c68b-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**INTRANET do URLZONE \_**</span><span class="sxs-lookup"><span data-stu-id="8c68b-116"><span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**URLZONE\_INTRANET**</span></span>


</dt> <dd>

<span data-ttu-id="8c68b-117">Zona usada para conteúdo encontrado em uma intranet.</span><span class="sxs-lookup"><span data-stu-id="8c68b-117">Zone used for content found on an intranet.</span></span>

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span data-ttu-id="8c68b-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE \_ confiável**</span><span class="sxs-lookup"><span data-stu-id="8c68b-118"><span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE\_TRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="8c68b-119">Zona usada para sites confiáveis na Internet.</span><span class="sxs-lookup"><span data-stu-id="8c68b-119">Zone used for trusted websites on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span data-ttu-id="8c68b-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**\_Internet UrlZone**</span><span class="sxs-lookup"><span data-stu-id="8c68b-120"><span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE\_INTERNET**</span></span>


</dt> <dd>

<span data-ttu-id="8c68b-121">Zona usada para a maior parte do conteúdo na Internet.</span><span class="sxs-lookup"><span data-stu-id="8c68b-121">Zone used for most of the content on the Internet.</span></span>

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span data-ttu-id="8c68b-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE \_ não confiável**</span><span class="sxs-lookup"><span data-stu-id="8c68b-122"><span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE\_UNTRUSTED**</span></span>


</dt> <dd>

<span data-ttu-id="8c68b-123">Zona usada para sites que não são confiáveis.</span><span class="sxs-lookup"><span data-stu-id="8c68b-123">Zone used for websites that are not trusted.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c68b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c68b-124">Requirements</span></span>



| <span data-ttu-id="8c68b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c68b-125">Requirement</span></span> | <span data-ttu-id="8c68b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8c68b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c68b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c68b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c68b-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c68b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c68b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c68b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c68b-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c68b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c68b-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c68b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c68b-132"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c68b-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
