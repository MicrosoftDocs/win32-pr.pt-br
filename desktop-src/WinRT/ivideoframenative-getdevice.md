---
description: Esse método retorna um dispositivo associado aos dados de vídeo.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Método IVideoFrameNative:: GetDevice'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370649"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="71572-103">Método IVideoFrameNative:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="71572-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="71572-104">Esse método retorna um dispositivo associado aos dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71572-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="71572-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71572-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="71572-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71572-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71572-107">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71572-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71572-108">O IID do dispositivo a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="71572-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="71572-109">*PPV* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="71572-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71572-110">Quando esse método retorna com êxito, contém o ponteiro do dispositivo solicitado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="71572-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71572-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71572-111">Return value</span></span>

<span data-ttu-id="71572-112">Retorna S \_ OK após a conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="71572-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="71572-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="71572-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71572-114">**IVideoFrameNative**</span><span class="sxs-lookup"><span data-stu-id="71572-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



