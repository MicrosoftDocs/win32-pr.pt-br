---
title: Propriedade IMsRdpClientShell2 MsRdpWorkspace
description: Recupera um ponteiro para a interface IMsRdpWorkspace, que é usada para gerenciar Conexão de RemoteApp e Área de Trabalho credenciais e conexões.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade MsRdpWorkspace
- Propriedade MsRdpWorkspace Serviços de Área de Trabalho Remota, interface IMsRdpClientShell2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell2, Propriedade MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644874"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="9bb28-106">Propriedade IMsRdpClientShell2:: MsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="9bb28-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="9bb28-107">Recupera um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , que é usada para gerenciar conexão de RemoteApp e área de trabalho credenciais e conexões.</span><span class="sxs-lookup"><span data-stu-id="9bb28-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="9bb28-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9bb28-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb28-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb28-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="9bb28-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9bb28-110">Property value</span></span>

<span data-ttu-id="9bb28-111">O endereço de um ponteiro para a interface [**IMsRdpWorkspace**](imsrdpworkspace.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb28-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb28-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bb28-112">Remarks</span></span>

<span data-ttu-id="9bb28-113">A interface [**IMsRdpWorkspace**](imsrdpworkspace.md) não é exposta como uma interface personalizada.</span><span class="sxs-lookup"><span data-stu-id="9bb28-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="9bb28-114">Ele só pode ser acessado por meio de métodos [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9bb28-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb28-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb28-115">Requirements</span></span>



| <span data-ttu-id="9bb28-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bb28-116">Requirement</span></span> | <span data-ttu-id="9bb28-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb28-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb28-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bb28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9bb28-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9bb28-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9bb28-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bb28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9bb28-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9bb28-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="9bb28-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9bb28-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bb28-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bb28-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb28-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9bb28-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb28-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="9bb28-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

