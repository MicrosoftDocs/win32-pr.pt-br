---
title: Método de fluxo de IDeviceIcon
description: Recupera o ícone como um fluxo.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- API de streaming de mídia do método de fluxo
- API de streaming de mídia do método de fluxo, interface IDeviceIcon
- API de streaming de mídia da interface IDeviceIcon, método de fluxo
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294043"
---
# <a name="ideviceiconstream-method"></a><span data-ttu-id="8a762-106">Método IDeviceIcon:: Stream</span><span class="sxs-lookup"><span data-stu-id="8a762-106">IDeviceIcon::Stream method</span></span>

<span data-ttu-id="8a762-107">Recupera o ícone como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="8a762-107">Retrieves the icon as a stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a762-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a762-108">Syntax</span></span>


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a><span data-ttu-id="8a762-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a762-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a762-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8a762-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a762-111">Recebe uma referência a um [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) que pode ser usado para recuperar os dados da imagem.</span><span class="sxs-lookup"><span data-stu-id="8a762-111">Receives a reference to a [**IRandomAccessStreamWithContentType**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) that can be used to retrieve the image data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a762-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a762-112">Return value</span></span>

<span data-ttu-id="8a762-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a762-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a762-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a762-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a762-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a762-115">Return code</span></span>                                                                          | <span data-ttu-id="8a762-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a762-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a762-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a762-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a762-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8a762-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8a762-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a762-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a762-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="8a762-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

