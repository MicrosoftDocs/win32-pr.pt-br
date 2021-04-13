---
description: Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.
ms.assetid: DF60C49A-89FE-4EEB-8E82-C2C43F2D2F2A
title: 'Método IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthProvider.GetPreferredEndpointTokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 670835ee3c2dfd01ae46a7cf78395959ea9a26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164610"
---
# <a name="iupdateendpointauthprovidergetpreferredendpointtokentype-method"></a><span data-ttu-id="c83fa-103">Método IUpdateEndpointAuthProvider:: GetPreferredEndpointTokenType</span><span class="sxs-lookup"><span data-stu-id="c83fa-103">IUpdateEndpointAuthProvider::GetPreferredEndpointTokenType method</span></span>

<span data-ttu-id="c83fa-104">Retorna o tipo preferencial de token de autenticação para o ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="c83fa-104">Returns the preferred type of authentication token for the endpoint of the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c83fa-105">Syntax</span></span>


```C++
HRESULT GetPreferredEndpointTokenType(
  [in]  GUID               serviceId,
  [in]  UpdateEndpointType endpointType,
  [in]  ULONG              ulRequestedTypes,
  [out] ULONG              *pulPreferredTokenTypes
);
```



## <a name="parameters"></a><span data-ttu-id="c83fa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c83fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83fa-107">*ServiceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-107">*serviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83fa-108">Identifica o serviço a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c83fa-108">Identifies the service to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="c83fa-109">*ponto de extremidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-109">*endpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83fa-110">Identifica o tipo de ponto de extremidade tneeded para se conectar ao serviço.</span><span class="sxs-lookup"><span data-stu-id="c83fa-110">Identifies the type of endpoint tneeded to connect to the service.</span></span>

</dd> <dt>

<span data-ttu-id="c83fa-111">*ulRequestedTypes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-111">*ulRequestedTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83fa-112">Identifica o conjunto de tokens com or sem suporte no ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c83fa-112">Identifies the ORed set of tokens that are supported by the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="c83fa-113">*pulPreferredTokenTypes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-113">*pulPreferredTokenTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c83fa-114">Especifique o conjunto de tipos de token de autenticação com or. preferencial.</span><span class="sxs-lookup"><span data-stu-id="c83fa-114">Specify the ORed set of authentication token types that are preferred.</span></span> <span data-ttu-id="c83fa-115">(Defina como 0 para indicar que nenhum token de autenticação é necessário).</span><span class="sxs-lookup"><span data-stu-id="c83fa-115">(Set to 0 to indicate that no authentication token is needed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83fa-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c83fa-116">Return value</span></span>

<span data-ttu-id="c83fa-117">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c83fa-117">Returns S\_OK if successful.</span></span> <span data-ttu-id="c83fa-118">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="c83fa-118">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c83fa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="c83fa-119">Remarks</span></span>

<span data-ttu-id="c83fa-120">Quando esse método é retornado, o WUA escolhe um tipo de token dos tipos preferenciais e o passa para o parâmetro TokenType do método [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) .</span><span class="sxs-lookup"><span data-stu-id="c83fa-120">When this method is returned, WUA chooses a token type from the preferred types and passes it to the tokenType parameter of the [**GetEndpointToken**](iupdateendpointauthprovider-getendpointtoken.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83fa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c83fa-121">Requirements</span></span>



| <span data-ttu-id="c83fa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83fa-122">Requirement</span></span> | <span data-ttu-id="c83fa-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c83fa-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83fa-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c83fa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c83fa-125">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="c83fa-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c83fa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c83fa-127">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="c83fa-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="c83fa-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c83fa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c83fa-129"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="c83fa-129"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="c83fa-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="c83fa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c83fa-131"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c83fa-131"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="c83fa-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c83fa-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c83fa-133"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c83fa-133"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="c83fa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c83fa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83fa-135"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c83fa-135"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c83fa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c83fa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83fa-137">**IUpdateEndpointAuthProvider**</span><span class="sxs-lookup"><span data-stu-id="c83fa-137">**IUpdateEndpointAuthProvider**</span></span>](iupdateendpointauthprovider.md)
</dt> <dt>

[<span data-ttu-id="c83fa-138">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="c83fa-138">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




