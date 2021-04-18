---
title: Enumeração TransportStatus
description: Define o status de transporte disponível conforme definido pelas diretrizes de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API de streaming de mídia de enumeração TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814533"
---
# <a name="transportstatus-enumeration"></a><span data-ttu-id="09ec7-104">Enumeração TransportStatus</span><span class="sxs-lookup"><span data-stu-id="09ec7-104">TransportStatus enumeration</span></span>

<span data-ttu-id="09ec7-105">Define o status de transporte disponível conforme definido pelas diretrizes de UPnP.</span><span class="sxs-lookup"><span data-stu-id="09ec7-105">Defines the available transport status as defined by the UPnP Guidelines.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ec7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09ec7-106">Syntax</span></span>


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a><span data-ttu-id="09ec7-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="09ec7-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="09ec7-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**</span><span class="sxs-lookup"><span data-stu-id="09ec7-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="09ec7-109">Status do dispositivo errôneo.</span><span class="sxs-lookup"><span data-stu-id="09ec7-109">Erroneous device status.</span></span>

</dd> <dt>

<span data-ttu-id="09ec7-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Okey**</span><span class="sxs-lookup"><span data-stu-id="09ec7-110"><span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**</span></span>
</dt> <dd>

<span data-ttu-id="09ec7-111">O dispositivo está em um bom status.</span><span class="sxs-lookup"><span data-stu-id="09ec7-111">The device is in a good status.</span></span>

</dd> <dt>

<span data-ttu-id="09ec7-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span><span class="sxs-lookup"><span data-stu-id="09ec7-112"><span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**</span></span>
</dt> <dd>

<span data-ttu-id="09ec7-113">Ocorreu um erro no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09ec7-113">An error occurred on the device.</span></span>

</dd> <dt>

<span data-ttu-id="09ec7-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**</span><span class="sxs-lookup"><span data-stu-id="09ec7-114"><span id="Last"></span><span id="last"></span><span id="LAST"></span>**Last**</span></span>
</dt> <dd>

<span data-ttu-id="09ec7-115">O status do dispositivo anterior para o status de transporte atual.</span><span class="sxs-lookup"><span data-stu-id="09ec7-115">The device s previous status to the current transport status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09ec7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09ec7-116">Requirements</span></span>



| <span data-ttu-id="09ec7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ec7-117">Requirement</span></span> | <span data-ttu-id="09ec7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="09ec7-118">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ec7-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="09ec7-119">IDL</span></span><br/> | <dl> <span data-ttu-id="09ec7-120"><dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="09ec7-120"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





