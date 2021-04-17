---
description: Obtém o identificador do serviço a ser autenticado com o token do ponto de extremidade.
ms.assetid: FE110B8E-F8FB-4CC8-BDD8-6427BA8B7920
title: 'Método IUpdateEndpointAuthToken:: ServiceId (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.ServiceID
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 8384baa0a4f8bb48e603e0f2f8bed417e783b7f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785206"
---
# <a name="iupdateendpointauthtokenserviceid-method"></a><span data-ttu-id="a98d7-103">Método IUpdateEndpointAuthToken:: ServiceId</span><span class="sxs-lookup"><span data-stu-id="a98d7-103">IUpdateEndpointAuthToken::ServiceID method</span></span>

<span data-ttu-id="a98d7-104">Obtém o identificador do serviço a ser autenticado com o token do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a98d7-104">Gets the identifier of the service to be authenticated with the endpoint token.</span></span>

## <a name="syntax"></a><span data-ttu-id="a98d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a98d7-105">Syntax</span></span>


```C++
HRESULT ServiceID(
  [out] GUID *pServiceID
);
```



## <a name="parameters"></a><span data-ttu-id="a98d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a98d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a98d7-107">*pServiceID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a98d7-107">*pServiceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a98d7-108">O identificador do serviço.</span><span class="sxs-lookup"><span data-stu-id="a98d7-108">The identifier of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a98d7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a98d7-109">Return value</span></span>

<span data-ttu-id="a98d7-110">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a98d7-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="a98d7-111">Caso contrário, retorna um código de erro COM do Windows.</span><span class="sxs-lookup"><span data-stu-id="a98d7-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98d7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a98d7-112">Requirements</span></span>



| <span data-ttu-id="a98d7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a98d7-113">Requirement</span></span> | <span data-ttu-id="a98d7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a98d7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98d7-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a98d7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a98d7-116">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="a98d7-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="a98d7-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a98d7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a98d7-118">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="a98d7-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a98d7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a98d7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a98d7-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="a98d7-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="a98d7-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="a98d7-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a98d7-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a98d7-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="a98d7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a98d7-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a98d7-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a98d7-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="a98d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a98d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a98d7-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a98d7-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a98d7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a98d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a98d7-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="a98d7-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




