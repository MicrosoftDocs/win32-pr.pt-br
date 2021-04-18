---
title: Propriedade IMsRdpClientShell2 SecuredSettingsEnabled
description: Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SecuredSettingsEnabled
- Propriedade SecuredSettingsEnabled Serviços de Área de Trabalho Remota, interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2, Propriedade SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753327"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a><span data-ttu-id="1222c-106">Propriedade IMsRdpClientShell2:: SecuredSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="1222c-106">IMsRdpClientShell2::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="1222c-107">Recupera um valor que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1222c-107">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

<span data-ttu-id="1222c-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="1222c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1222c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1222c-109">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="1222c-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1222c-110">Property value</span></span>

<span data-ttu-id="1222c-111">Um ponteiro para um valor booliano que indica se a página da Web atual está em uma zona de segurança de URL confiável do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1222c-111">A pointer to a Boolean value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span>

## <a name="requirements"></a><span data-ttu-id="1222c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1222c-112">Requirements</span></span>



| <span data-ttu-id="1222c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1222c-113">Requirement</span></span> | <span data-ttu-id="1222c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1222c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1222c-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1222c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1222c-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1222c-116">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1222c-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1222c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1222c-118">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1222c-118">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="1222c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1222c-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1222c-120"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1222c-120"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1222c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="1222c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1222c-122">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="1222c-122">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

 





