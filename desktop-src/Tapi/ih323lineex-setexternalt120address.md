---
description: O método SetExternalT120Address é chamado por um aplicativo para configurar um endereço T. 120 externo para troca de dados.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'Método IH323LineEx:: SetExternalT120Address (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760345"
---
# <a name="ih323lineexsetexternalt120address-method"></a><span data-ttu-id="86761-103">Método IH323LineEx:: SetExternalT120Address</span><span class="sxs-lookup"><span data-stu-id="86761-103">IH323LineEx::SetExternalT120Address method</span></span>

<span data-ttu-id="86761-104">\[O **SetExternalT120Address** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="86761-104">\[**SetExternalT120Address** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86761-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="86761-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86761-106">O método **SetExternalT120Address** é chamado por um aplicativo para configurar um endereço T. 120 externo para troca de dados.</span><span class="sxs-lookup"><span data-stu-id="86761-106">The **SetExternalT120Address** method is called by an application to configure an external T.120 address for data exchange.</span></span> <span data-ttu-id="86761-107">A funcionalidade T. 120 será anunciada durante a negociação H. 245 e o endereço será usado na confirmação do canal de lógica aberta para que o outro ponto de extremidade possa configurar sessões T. 120 com o serviço de escuta nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="86761-107">T.120 capability will be advertised during the H.245 negotiation, and the address will be used in the open logic channel acknowledgement so that the other endpoint can set up T.120 sessions with the service listening on that address.</span></span> <span data-ttu-id="86761-108">Se essa função não for chamada, o provedor de serviços H. 323 não anunciará a funcionalidade T. 120.</span><span class="sxs-lookup"><span data-stu-id="86761-108">If this function is not called, the H.323 service provider will not advertise T.120 capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="86761-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86761-109">Syntax</span></span>


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a><span data-ttu-id="86761-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86761-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86761-111">*fEnable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86761-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86761-112">**True** para habilitar a funcionalidade T. 120; **False** para desabilitar a funcionalidade T. 120.</span><span class="sxs-lookup"><span data-stu-id="86761-112">**TRUE** to enable T.120 capability; **FALSE** to disable T.120 capability.</span></span>

</dd> <dt>

<span data-ttu-id="86761-113">*dwIP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86761-113">*dwIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86761-114">**DWORD** que contém o endereço IP na ordem de bytes do host do serviço externo T. 120.</span><span class="sxs-lookup"><span data-stu-id="86761-114">**DWORD** containing the IP address in host byte order of the external T.120 service.</span></span>

</dd> <dt>

<span data-ttu-id="86761-115">*wPort* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86761-115">*wPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86761-116">O **Word** que contém a porta do serviço T. 120 externo.</span><span class="sxs-lookup"><span data-stu-id="86761-116">**WORD** containing the port of the external T.120 service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86761-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86761-117">Return value</span></span>

<span data-ttu-id="86761-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="86761-118">This method can return one of these values.</span></span>



| <span data-ttu-id="86761-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="86761-119">Return code</span></span>                                                                          | <span data-ttu-id="86761-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="86761-120">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="86761-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86761-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="86761-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="86761-122">Method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="86761-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86761-123">Requirements</span></span>



| <span data-ttu-id="86761-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="86761-124">Requirement</span></span> | <span data-ttu-id="86761-125">Valor</span><span class="sxs-lookup"><span data-stu-id="86761-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86761-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="86761-126">TAPI version</span></span><br/> | <span data-ttu-id="86761-127">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="86761-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86761-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86761-128">Header</span></span><br/>       | <dl> <span data-ttu-id="86761-129"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="86761-129"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="86761-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86761-130">Library</span></span><br/>      | <dl> <span data-ttu-id="86761-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86761-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86761-132">DLL</span><span class="sxs-lookup"><span data-stu-id="86761-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="86761-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86761-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




