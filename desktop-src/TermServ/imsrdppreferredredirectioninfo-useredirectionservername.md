---
title: Propriedade IMsRdpPreferredRedirectionInfo UseRedirectionServerName
description: Obtém e define se deve ser usado o nome do servidor de redirecionamento.
ms.assetid: D2239600-D75D-40FB-A6D0-4C7C4C5163E3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade UseRedirectionServerName
- Propriedade UseRedirectionServerName Serviços de Área de Trabalho Remota, interface IMsRdpPreferredRedirectionInfo
- Serviços de Área de Trabalho Remota de interface IMsRdpPreferredRedirectionInfo, Propriedade UseRedirectionServerName
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo.UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.get_UseRedirectionServerName
- IMsRdpPreferredRedirectionInfo.put_UseRedirectionServerName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1635273078a2d09ca01c219ebf7eaa482eeb7a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644464"
---
# <a name="imsrdppreferredredirectioninfouseredirectionservername-property"></a><span data-ttu-id="26109-106">Propriedade IMsRdpPreferredRedirectionInfo:: UseRedirectionServerName</span><span class="sxs-lookup"><span data-stu-id="26109-106">IMsRdpPreferredRedirectionInfo::UseRedirectionServerName property</span></span>

<span data-ttu-id="26109-107">Obtém e define se deve ser usado o nome do servidor de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="26109-107">Gets and sets whether to use the redirection server name.</span></span>

<span data-ttu-id="26109-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="26109-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="26109-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26109-109">Syntax</span></span>


```C++
HRESULT put_UseRedirectionServerName(
  [in]  VARIANT_BOOL UseRedirectionServerName
);

HRESULT get_UseRedirectionServerName(
  [out] VARIANT_BOOL *UseRedirectionServerName
);
```



## <a name="property-value"></a><span data-ttu-id="26109-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="26109-110">Property value</span></span>

<span data-ttu-id="26109-111">Se deve ser usado o nome do servidor de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="26109-111">Whether to use the redirection server name.</span></span>

## <a name="requirements"></a><span data-ttu-id="26109-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26109-112">Requirements</span></span>



| <span data-ttu-id="26109-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="26109-113">Requirement</span></span> | <span data-ttu-id="26109-114">Valor</span><span class="sxs-lookup"><span data-stu-id="26109-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26109-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26109-115">Minimum supported client</span></span><br/> | <span data-ttu-id="26109-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="26109-116">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="26109-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26109-117">Minimum supported server</span></span><br/> | <span data-ttu-id="26109-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26109-118">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="26109-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="26109-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="26109-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26109-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="26109-121">DLL</span><span class="sxs-lookup"><span data-stu-id="26109-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26109-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26109-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="26109-123">IID</span><span class="sxs-lookup"><span data-stu-id="26109-123">IID</span></span><br/>                      | <span data-ttu-id="26109-124">IID \_ IMsRdpPreferredRedirectionInfo é definido como FDD029F9-9574-4DEF-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="26109-124">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26109-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="26109-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26109-126">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="26109-126">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)
</dt> </dl>

 

 





