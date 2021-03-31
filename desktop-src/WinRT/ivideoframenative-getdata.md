---
description: Esse método retorna uma interface que fornece acesso aos dados de vídeo.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Método IVideoFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920914"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="2c131-103">Método IVideoFrameNative:: GetData</span><span class="sxs-lookup"><span data-stu-id="2c131-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="2c131-104">Esse método retorna uma interface que fornece acesso aos dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2c131-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c131-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c131-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="2c131-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c131-107">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2c131-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c131-108">O IID da interface a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="2c131-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2c131-109">*PPV* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c131-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c131-110">Quando esse método retorna com êxito, contém o ponteiro de interface solicitado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="2c131-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c131-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c131-111">Return value</span></span>

<span data-ttu-id="2c131-112">Retorna S \_ OK após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2c131-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="2c131-113">Retorna E \_ nointerface se a interface solicitada não puder ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="2c131-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c131-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c131-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c131-115">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="2c131-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



