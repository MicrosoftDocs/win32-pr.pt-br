---
description: Esse método retorna uma interface que fornece acesso aos dados de áudio.
ms.assetid: 4FA7CC9D-D379-4C08-8D4F-5301ECCDF372
title: 'Método IAudioFrameNative:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAudioFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: eb61bce5132c2029b6f53fdd1159ca50984ba936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090415"
---
# <a name="iaudioframenativegetdata-method"></a><span data-ttu-id="68d4d-103">Método IAudioFrameNative:: GetData</span><span class="sxs-lookup"><span data-stu-id="68d4d-103">IAudioFrameNative::GetData method</span></span>

<span data-ttu-id="68d4d-104">Esse método retorna uma interface que fornece acesso aos dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="68d4d-104">This method returns an interface that provides access to the audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68d4d-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="68d4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68d4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d4d-107">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68d4d-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d4d-108">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="68d4d-108">Type: **REFIID**</span></span>

<span data-ttu-id="68d4d-109">O IID da interface a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="68d4d-109">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="68d4d-110">*PPV* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="68d4d-110">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68d4d-111">Tipo: \**LPVOID \** _</span><span class="sxs-lookup"><span data-stu-id="68d4d-111">Type: \**LPVOID\** _</span></span>

<span data-ttu-id="68d4d-112">Quando esse método retorna com êxito, contém o ponteiro de interface solicitado no parâmetro _riid \*.</span><span class="sxs-lookup"><span data-stu-id="68d4d-112">When this method returns successfully, contains the interface pointer requested in _riid\* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68d4d-113">Return value</span></span>

<span data-ttu-id="68d4d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68d4d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68d4d-115">Retorna S \_ OK após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="68d4d-115">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="68d4d-116">Retorna E \_ nointerface se a interface solicitada não puder ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="68d4d-116">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="68d4d-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="68d4d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d4d-118">**IAudioFrameNative**</span><span class="sxs-lookup"><span data-stu-id="68d4d-118">**IAudioFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative)
</dt> </dl>

 

 



