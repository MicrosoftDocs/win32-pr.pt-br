---
title: Método IMsRdpCameraRedirConfigCollection AddConfig
description: Adiciona um objeto IMsRdpCameraRedirConfig à coleção (a câmera correspondente não precisa estar conectada).
ms.tgt_platform: multiple
keywords:
- Método addconfig Serviços de Área de Trabalho Remota
- Método addconfig Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota, método addconfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104500113"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="f2c26-106">Método IMsRdpCameraRedirConfigCollection:: addconfig</span><span class="sxs-lookup"><span data-stu-id="f2c26-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="f2c26-107">Adiciona um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à coleção (a câmera correspondente não precisa estar conectada).</span><span class="sxs-lookup"><span data-stu-id="f2c26-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2c26-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2c26-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="f2c26-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2c26-109">Parameters</span></span>

<span data-ttu-id="f2c26-110">*symbolicLink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2c26-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="f2c26-111">O link simbólico para o novo objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f2c26-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="f2c26-112">*fRedirected* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2c26-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="f2c26-113">Especifica se a nova câmera será redirecionada por padrão.</span><span class="sxs-lookup"><span data-stu-id="f2c26-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2c26-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2c26-114">Return value</span></span>

<span data-ttu-id="f2c26-115">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f2c26-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2c26-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2c26-116">Requirements</span></span>

| <span data-ttu-id="f2c26-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2c26-117">Requirement</span></span> | <span data-ttu-id="f2c26-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f2c26-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f2c26-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2c26-119">Minimum supported client</span></span>| <span data-ttu-id="f2c26-120">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="f2c26-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f2c26-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f2c26-121">Type library</span></span>            | <span data-ttu-id="f2c26-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f2c26-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f2c26-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f2c26-123">DLL</span></span>                  | <span data-ttu-id="f2c26-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f2c26-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f2c26-125">IID</span><span class="sxs-lookup"><span data-stu-id="f2c26-125">IID</span></span>                      | <span data-ttu-id="f2c26-126">IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="f2c26-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f2c26-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2c26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2c26-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="f2c26-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>