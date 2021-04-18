---
title: Enumeração ConnectionStatus
description: Representa o estado do dispositivo na rede como visto pela última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API de streaming de mídia de enumeração ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793926"
---
# <a name="connectionstatus-enumeration"></a><span data-ttu-id="34444-104">Enumeração ConnectionStatus</span><span class="sxs-lookup"><span data-stu-id="34444-104">ConnectionStatus enumeration</span></span>

<span data-ttu-id="34444-105">Representa o estado do dispositivo na rede como visto pela última vez.</span><span class="sxs-lookup"><span data-stu-id="34444-105">Represents the state of the device in the network as last seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="34444-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="34444-106">Syntax</span></span>


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a><span data-ttu-id="34444-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="34444-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="34444-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Conectar**</span><span class="sxs-lookup"><span data-stu-id="34444-108"><span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**</span></span>
</dt> <dd>

<span data-ttu-id="34444-109">O dispositivo está online e ativo na rede.</span><span class="sxs-lookup"><span data-stu-id="34444-109">Device is online and active on the network.</span></span>

</dd> <dt>

<span data-ttu-id="34444-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Está**</span><span class="sxs-lookup"><span data-stu-id="34444-110"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**</span></span>
</dt> <dd>

<span data-ttu-id="34444-111">O dispositivo está offline.</span><span class="sxs-lookup"><span data-stu-id="34444-111">Device is offline.</span></span>

</dd> <dt>

<span data-ttu-id="34444-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Dormindo**</span><span class="sxs-lookup"><span data-stu-id="34444-112"><span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Sleeping**</span></span>
</dt> <dd>

<span data-ttu-id="34444-113">O dispositivo está offline no momento, mas pode ser ativado automaticamente quando for feita uma tentativa de comunicação com ele.</span><span class="sxs-lookup"><span data-stu-id="34444-113">Device is currently offline but might automatically wake up when an attempt is made to communicate with it.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34444-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34444-114">Requirements</span></span>



| <span data-ttu-id="34444-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="34444-115">Requirement</span></span> | <span data-ttu-id="34444-116">Valor</span><span class="sxs-lookup"><span data-stu-id="34444-116">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34444-117">INSERI</span><span class="sxs-lookup"><span data-stu-id="34444-117">IDL</span></span><br/> | <dl> <span data-ttu-id="34444-118"><dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="34444-118"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





