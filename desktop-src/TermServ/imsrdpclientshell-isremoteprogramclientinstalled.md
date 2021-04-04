---
title: Propriedade IMsRdpClientShell IsRemoteProgramClientInstalled
description: Recupera se o cliente de Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade do RemoteApp do Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade IsRemoteProgramClientInstalled
- Propriedade IsRemoteProgramClientInstalled Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell, Propriedade IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085358"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="36d12-106">Propriedade IMsRdpClientShell:: IsRemoteProgramClientInstalled</span><span class="sxs-lookup"><span data-stu-id="36d12-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="36d12-107">Recupera se o cliente de Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade do RemoteApp do Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="36d12-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="36d12-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="36d12-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d12-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36d12-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="36d12-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="36d12-110">Property value</span></span>

<span data-ttu-id="36d12-111">Recupera se o cliente de Conexão de Área de Trabalho Remota (RDC) dá suporte à funcionalidade do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="36d12-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d12-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36d12-112">Requirements</span></span>



| <span data-ttu-id="36d12-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="36d12-113">Requirement</span></span> | <span data-ttu-id="36d12-114">Valor</span><span class="sxs-lookup"><span data-stu-id="36d12-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d12-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36d12-115">Minimum supported client</span></span><br/> | <span data-ttu-id="36d12-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36d12-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="36d12-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36d12-117">Minimum supported server</span></span><br/> | <span data-ttu-id="36d12-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36d12-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="36d12-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="36d12-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="36d12-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d12-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="36d12-121">DLL</span><span class="sxs-lookup"><span data-stu-id="36d12-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d12-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d12-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="36d12-123">IID</span><span class="sxs-lookup"><span data-stu-id="36d12-123">IID</span></span><br/>                      | <span data-ttu-id="36d12-124">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="36d12-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="36d12-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="36d12-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d12-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="36d12-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





