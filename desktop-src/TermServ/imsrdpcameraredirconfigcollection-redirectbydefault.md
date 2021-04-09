---
title: Propriedade IMsRdpCameraRedirConfigCollection RedirectByDefault
description: Especifica se uma nova câmera será redirecionada por padrão.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RedirectByDefault
- Propriedade RedirectByDefault Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087194"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="d2764-106">Propriedade IMsRdpCameraRedirConfigCollection:: RedirectByDefault</span><span class="sxs-lookup"><span data-stu-id="d2764-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="d2764-107">Especifica se uma nova câmera será redirecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d2764-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="d2764-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d2764-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2764-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2764-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="d2764-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d2764-110">Property value</span></span>

<span data-ttu-id="d2764-111">Um valor que indica se uma nova câmera é redirecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="d2764-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2764-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2764-112">Requirements</span></span>

| <span data-ttu-id="d2764-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2764-113">Requirement</span></span> | <span data-ttu-id="d2764-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d2764-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d2764-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2764-115">Minimum supported client</span></span>| <span data-ttu-id="d2764-116">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="d2764-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d2764-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d2764-117">Type library</span></span>            | <span data-ttu-id="d2764-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d2764-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d2764-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d2764-119">DLL</span></span>                  | <span data-ttu-id="d2764-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d2764-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d2764-121">IID</span><span class="sxs-lookup"><span data-stu-id="d2764-121">IID</span></span>                      | <span data-ttu-id="d2764-122">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="d2764-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="d2764-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2764-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2764-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="d2764-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>