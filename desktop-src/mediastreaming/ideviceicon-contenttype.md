---
title: Método ContentType IDeviceIcon
description: Recupera o tipo de conteúdo do ícone.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- API de streaming de mídia do método ContentType
- API de streaming de mídia do método ContentType, interface IDeviceIcon
- API de streaming de mídia da interface IDeviceIcon, método ContentType
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823690"
---
# <a name="ideviceiconcontenttype-method"></a><span data-ttu-id="09df2-106">Método IDeviceIcon:: ContentType</span><span class="sxs-lookup"><span data-stu-id="09df2-106">IDeviceIcon::ContentType method</span></span>

<span data-ttu-id="09df2-107">Recupera o tipo de conteúdo do ícone.</span><span class="sxs-lookup"><span data-stu-id="09df2-107">Retrieves the content type of the icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="09df2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09df2-108">Syntax</span></span>


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="09df2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09df2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09df2-110">*valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="09df2-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09df2-111">Recebe um ponteiro para o tipo de conteúdo do ícone.</span><span class="sxs-lookup"><span data-stu-id="09df2-111">Receives a pointer to the content type of the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09df2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09df2-112">Return value</span></span>

<span data-ttu-id="09df2-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="09df2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="09df2-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="09df2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="09df2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="09df2-115">Return code</span></span>                                                                          | <span data-ttu-id="09df2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="09df2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="09df2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09df2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="09df2-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="09df2-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="09df2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="09df2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09df2-120">**IDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="09df2-120">**IDeviceIcon**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

