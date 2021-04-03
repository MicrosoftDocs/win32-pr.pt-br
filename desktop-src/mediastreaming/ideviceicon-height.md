---
title: Método de altura de IDeviceIcon
description: Recupera a altura do ícone em pixels.
ms.assetid: 06E1B3AD-FF49-4BC9-AC67-E2E00954475F
keywords:
- API de streaming de mídia do método de altura
- Método Height API de streaming de mídia, interface IDeviceIcon
- API de streaming de mídia da interface IDeviceIcon, método Height
topic_type:
- apiref
api_name:
- IDeviceIcon.Height
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdba8d107cc844a29d215e5da49949595a8cd27a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007537"
---
# <a name="ideviceiconheight-method"></a><span data-ttu-id="04846-106">Método IDeviceIcon:: Height</span><span class="sxs-lookup"><span data-stu-id="04846-106">IDeviceIcon::Height method</span></span>

<span data-ttu-id="04846-107">Recupera a altura do ícone em pixels.</span><span class="sxs-lookup"><span data-stu-id="04846-107">Retrieves the height of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="04846-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04846-108">Syntax</span></span>


```C++
HRESULT Height(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="04846-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04846-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04846-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="04846-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04846-111">Recebe um ponteiro para a altura do ícone em pixels.</span><span class="sxs-lookup"><span data-stu-id="04846-111">Receives a pointer to the height of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04846-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04846-112">Return value</span></span>

<span data-ttu-id="04846-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="04846-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="04846-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="04846-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="04846-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="04846-115">Return code</span></span>                                                                          | <span data-ttu-id="04846-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="04846-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="04846-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04846-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="04846-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="04846-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="04846-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="04846-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04846-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="04846-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

