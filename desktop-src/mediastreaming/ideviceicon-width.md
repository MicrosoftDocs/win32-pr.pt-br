---
title: Método de largura IDeviceIcon
description: Recupera a largura do ícone em pixels.
ms.assetid: 28ADA921-6808-43B8-966E-BA42B1B52931
keywords:
- API de streaming de mídia de método de largura
- API de streaming de mídia de método de largura, interface IDeviceIcon
- API de streaming de mídia da interface IDeviceIcon, método de largura
topic_type:
- apiref
api_name:
- IDeviceIcon.Width
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4b04f8c40cc209ccf1261af0fc2f6cdfd329db88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294042"
---
# <a name="ideviceiconwidth-method"></a><span data-ttu-id="b3400-106">Método IDeviceIcon:: Width</span><span class="sxs-lookup"><span data-stu-id="b3400-106">IDeviceIcon::Width method</span></span>

<span data-ttu-id="b3400-107">Recupera a largura do ícone em pixels.</span><span class="sxs-lookup"><span data-stu-id="b3400-107">Retrieves the width of the icon in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3400-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3400-108">Syntax</span></span>


```C++
HRESULT Width(
  [out] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="b3400-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3400-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3400-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b3400-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3400-111">Recebe um ponteiro para a largura do ícone em pixels.</span><span class="sxs-lookup"><span data-stu-id="b3400-111">Receives a pointer to the width of the icon in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3400-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3400-112">Return value</span></span>

<span data-ttu-id="b3400-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b3400-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b3400-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b3400-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b3400-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b3400-115">Return code</span></span>                                                                          | <span data-ttu-id="b3400-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b3400-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b3400-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b3400-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b3400-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b3400-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b3400-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3400-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3400-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="b3400-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

