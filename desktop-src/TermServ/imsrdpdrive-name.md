---
title: Propriedade de nome IMsRdpDrive
description: Recupera o nome da unidade.
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de nome
- Propriedade Name Serviços de Área de Trabalho Remota, interface IMsRdpDrive
- Serviços de Área de Trabalho Remota de interface IMsRdpDrive, Propriedade Name
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38eeb0f6112983f508bb43ba69d721aeb52c314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455487"
---
# <a name="imsrdpdrivename-property"></a><span data-ttu-id="de366-106">Propriedade IMsRdpDrive:: Name</span><span class="sxs-lookup"><span data-stu-id="de366-106">IMsRdpDrive::Name property</span></span>

<span data-ttu-id="de366-107">Recupera o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="de366-107">Retrieves the name of the drive.</span></span>

<span data-ttu-id="de366-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="de366-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de366-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de366-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a><span data-ttu-id="de366-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="de366-110">Property value</span></span>

<span data-ttu-id="de366-111">O nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="de366-111">The drive name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="de366-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="de366-112">Error codes</span></span>

<span data-ttu-id="de366-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="de366-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="de366-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="de366-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="de366-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de366-115">Requirements</span></span>



| <span data-ttu-id="de366-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de366-116">Requirement</span></span> | <span data-ttu-id="de366-117">Valor</span><span class="sxs-lookup"><span data-stu-id="de366-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de366-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de366-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de366-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de366-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="de366-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de366-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de366-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de366-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="de366-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="de366-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="de366-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de366-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="de366-124">DLL</span><span class="sxs-lookup"><span data-stu-id="de366-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de366-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de366-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="de366-126">IID</span><span class="sxs-lookup"><span data-stu-id="de366-126">IID</span></span><br/>                      | <span data-ttu-id="de366-127">IID \_ IMsRdpDrive é definido como d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="de366-127">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="de366-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="de366-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de366-129">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="de366-129">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

 





