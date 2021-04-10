---
description: Conecte-se a outra instância de um mecanismo remoto no computador local.
MS-HAID: vspixengine.IServerConnectionCallback\_ConnectToEngine\_BOOL\_BSTR\_IPixEngine\_ptr\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IServerConnectionCallback:: ConnectToEngine'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 56D67449-EA8B-4AD0-94D7-B3CDB7F0ABC8
api_name:
- IServerConnectionCallback.ConnectToEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1506075066767cba95c7fec768fa27e858bd6a10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087885"
---
# <a name="span-idvspixengineiserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptrspaniserverconnectioncallbackconnecttoengine-method"></a><span data-ttu-id="cbfac-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>Método IServerConnectionCallback:: ConnectToEngine</span><span class="sxs-lookup"><span data-stu-id="cbfac-103"><span id="vspixengine.iserverconnectioncallback_connecttoengine_bool_bstr_ipixengine_ptr_ptr"></span>IServerConnectionCallback::ConnectToEngine method</span></span>

<span data-ttu-id="cbfac-104">Conecte-se a outra instância de um mecanismo remoto no computador local.</span><span class="sxs-lookup"><span data-stu-id="cbfac-104">Connect to another instance of a remote engine on the local machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbfac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbfac-105">Syntax</span></span>


```C++
HRESULT ConnectToEngine(
   BOOL          bLegacyConnection,
   BSTR          runAddress,
   IPixEngine ** ppEngineCreated
);
```

## <a name="parameters"></a><span data-ttu-id="cbfac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbfac-106">Parameters</span></span>

<span data-ttu-id="cbfac-107">*bLegacyConnection* </span><span class="sxs-lookup"><span data-stu-id="cbfac-107">*bLegacyConnection* </span></span>  
<span data-ttu-id="cbfac-108">true se o mecanismo usar for herdado, caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="cbfac-108">true if the engine uses is legacy, otherwise false.</span></span>

<span data-ttu-id="cbfac-109">*runAddress* </span><span class="sxs-lookup"><span data-stu-id="cbfac-109">*runAddress* </span></span>  
<span data-ttu-id="cbfac-110">Uma cadeia de caracteres COM que contém o nome do computador local.</span><span class="sxs-lookup"><span data-stu-id="cbfac-110">A COM string containing the name of the local machine.</span></span>

<span data-ttu-id="cbfac-111">*ppEngineCreated* </span><span class="sxs-lookup"><span data-stu-id="cbfac-111">*ppEngineCreated* </span></span>  
<span data-ttu-id="cbfac-112">No retorno, o endereço da instância do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="cbfac-112">On return, the address of the engine instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbfac-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbfac-113">Return value</span></span>

<span data-ttu-id="cbfac-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cbfac-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cbfac-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbfac-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbfac-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cbfac-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbfac-117">Header</span></span></p></td><td><span data-ttu-id="cbfac-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cbfac-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cbfac-119"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="cbfac-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cbfac-120">**IServerConnectionCallback**</span><span class="sxs-lookup"><span data-stu-id="cbfac-120">**IServerConnectionCallback**</span></span>](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
