---
description: As constantes a seguir podem ser retornadas como erros.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes de RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779300"
---
# <a name="rnd_-constants"></a><span data-ttu-id="e9b61-103">Constantes de RND \_</span><span class="sxs-lookup"><span data-stu-id="e9b61-103">RND\_ Constants</span></span>

<span data-ttu-id="e9b61-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e9b61-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9b61-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="e9b61-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9b61-106">As constantes a seguir podem ser retornadas como erros.</span><span class="sxs-lookup"><span data-stu-id="e9b61-106">The following constants may be returned as errors.</span></span>

<dl> <dt>

<span data-ttu-id="e9b61-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_hora inválida do Rnd \_**</span><span class="sxs-lookup"><span data-stu-id="e9b61-107"><span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9b61-108">0xe0000200</span><span class="sxs-lookup"><span data-stu-id="e9b61-108">0xe0000200</span></span>
</dt> <dt>



<span data-ttu-id="e9b61-109">O valor de hora inserido não é válido.</span><span class="sxs-lookup"><span data-stu-id="e9b61-109">The time value entered is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b61-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**\_ \_ nome do servidor nulo do Rnd \_**</span><span class="sxs-lookup"><span data-stu-id="e9b61-110"><span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND\_NULL\_SERVER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9b61-111">0xe0000201</span><span class="sxs-lookup"><span data-stu-id="e9b61-111">0xe0000201</span></span>
</dt> <dt>



<span data-ttu-id="e9b61-112">O nome do servidor é **nulo**, provavelmente porque [**ITConferenceBlob:: init**](itconferenceblob-init.md) não foi executado ou não foi bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="e9b61-112">The server name is **NULL**, probably because [**ITConferenceBlob::Init**](itconferenceblob-init.md) has not been run or did not succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b61-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**o RND \_ já \_ está conectado**</span><span class="sxs-lookup"><span data-stu-id="e9b61-113"><span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9b61-114">0xe0000202</span><span class="sxs-lookup"><span data-stu-id="e9b61-114">0xe0000202</span></span>
</dt> <dt>



<span data-ttu-id="e9b61-115">O método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) foi chamado, mas já existe uma conexão.</span><span class="sxs-lookup"><span data-stu-id="e9b61-115">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method was called, but a connection already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e9b61-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ não \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="e9b61-116"><span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="e9b61-117">0xe0000203</span><span class="sxs-lookup"><span data-stu-id="e9b61-117">0xe0000203</span></span>
</dt> <dt>



<span data-ttu-id="e9b61-118">O método [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) não foi chamado ou falhou.</span><span class="sxs-lookup"><span data-stu-id="e9b61-118">The [**ITDirectory::Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) method has not been called, or failed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9b61-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9b61-119">Requirements</span></span>



| <span data-ttu-id="e9b61-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9b61-120">Requirement</span></span> | <span data-ttu-id="e9b61-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e9b61-121">Value</span></span> |
|-------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b61-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="e9b61-122">TAPI version</span></span><br/> | <span data-ttu-id="e9b61-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e9b61-123">Requires TAPI 3.0 or later</span></span><br/>                                               |
| <span data-ttu-id="e9b61-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9b61-124">Header</span></span><br/>       | <dl> <span data-ttu-id="e9b61-125"><dt>Rnderr. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b61-125"><dt>Rnderr.h</dt></span></span> </dl> |



 

 




