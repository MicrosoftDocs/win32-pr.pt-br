---
title: Propriedade de redirecionamento IMsRdpDrive
description: Indica o estado de redirecionamento da unidade.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Propriedade redirectionstate Serviços de Área de Trabalho Remota
- Propriedade redirectionstate Serviços de Área de Trabalho Remota, interface IMsRdpDrive
- Serviços de Área de Trabalho Remota de interface IMsRdpDrive, Propriedade redirectionstate
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561190e976e0b8190553376f5e9f7a5b2de2550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369779"
---
# <a name="imsrdpdriveredirectionstate-property"></a><span data-ttu-id="a903b-106">Propriedade IMsRdpDrive:: redirectionstate</span><span class="sxs-lookup"><span data-stu-id="a903b-106">IMsRdpDrive::RedirectionState property</span></span>

<span data-ttu-id="a903b-107">Indica o estado de redirecionamento da unidade.</span><span class="sxs-lookup"><span data-stu-id="a903b-107">Indicates the redirection state of the drive.</span></span>

<span data-ttu-id="a903b-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a903b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a903b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a903b-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="a903b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a903b-110">Property value</span></span>

<span data-ttu-id="a903b-111">Defina esse parâmetro como **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="a903b-111">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="a903b-112">para desabilitar o redirecionamento ou a **variante \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a903b-112">to disable redirection or **VARIANT\_TRUE**.</span></span> <span data-ttu-id="a903b-113">para habilitar o redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a903b-113">to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a903b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a903b-114">Error codes</span></span>

<span data-ttu-id="a903b-115">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="a903b-115">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="a903b-116">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="a903b-116">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a903b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a903b-117">Requirements</span></span>



| <span data-ttu-id="a903b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a903b-118">Requirement</span></span> | <span data-ttu-id="a903b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a903b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a903b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a903b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a903b-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a903b-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a903b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a903b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a903b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a903b-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a903b-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a903b-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="a903b-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a903b-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a903b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a903b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a903b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a903b-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a903b-128">IID</span><span class="sxs-lookup"><span data-stu-id="a903b-128">IID</span></span><br/>                      | <span data-ttu-id="a903b-129">IID \_ IMsRdpDrive é definido como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="a903b-129">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a903b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a903b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a903b-131">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="a903b-131">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





