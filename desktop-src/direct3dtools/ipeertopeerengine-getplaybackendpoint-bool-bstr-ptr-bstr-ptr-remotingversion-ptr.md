---
description: Obtém o endereço do ponto de extremidade de um mecanismo remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_GetPlaybackEndpoint\_BOOL\_BSTR\_ptr\_BSTR\_ptr\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPeerToPeerEngine:: GetPlaybackEndpoint'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3B391048-E7F7-4DA7-96A3-05875B170DCA
api_name:
- IPeerToPeerEngine.GetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6ee25dbd456086227e88fcb8bf7708a39e26eb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500323"
---
# <a name="span-idvspixengineipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptrspanipeertopeerenginegetplaybackendpoint-method"></a><span data-ttu-id="ba82c-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>Método IPeerToPeerEngine:: GetPlaybackEndpoint</span><span class="sxs-lookup"><span data-stu-id="ba82c-103"><span id="vspixengine.ipeertopeerengine_getplaybackendpoint_bool_bstr_ptr_bstr_ptr_remotingversion_ptr"></span>IPeerToPeerEngine::GetPlaybackEndpoint method</span></span>

<span data-ttu-id="ba82c-104">Obtém o endereço do ponto de extremidade de um mecanismo remoto.</span><span class="sxs-lookup"><span data-stu-id="ba82c-104">Gets the endpoint address of a remote engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba82c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba82c-105">Syntax</span></span>


```C++
HRESULT GetPlaybackEndpoint(
   BOOL              bUseAuthentication,
   BSTR *            pEndpoint,
   BSTR *            sessionKey,
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="ba82c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba82c-106">Parameters</span></span>

<span data-ttu-id="ba82c-107">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="ba82c-107">*bUseAuthentication* </span></span>  
<span data-ttu-id="ba82c-108">true se o mecanismo remoto usar autenticação; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="ba82c-108">true if the remote engine uses authentication; otherwise, false.</span></span>

<span data-ttu-id="ba82c-109">*pEndpoint* </span><span class="sxs-lookup"><span data-stu-id="ba82c-109">*pEndpoint* </span></span>  
<span data-ttu-id="ba82c-110">No retorno, uma cadeia de caracteres COM que contém o endereço do ponto de extremidade do computador de reprodução remota.</span><span class="sxs-lookup"><span data-stu-id="ba82c-110">On return, a COM string containing the endpoint address of the remote playback machine.</span></span>

<span data-ttu-id="ba82c-111">*sessionKey* </span><span class="sxs-lookup"><span data-stu-id="ba82c-111">*sessionKey* </span></span>  
<span data-ttu-id="ba82c-112">No retorno, uma cadeia de caracteres COM que contém a chave de sessão usada para criptografia.</span><span class="sxs-lookup"><span data-stu-id="ba82c-112">On return, a COM string containing the session key used for encryption.</span></span>

<span data-ttu-id="ba82c-113">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="ba82c-113">*pRemoteVersion* </span></span>  
<span data-ttu-id="ba82c-114">No retorno, a versão do mecanismo remoto.</span><span class="sxs-lookup"><span data-stu-id="ba82c-114">On return, the version of the remote engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba82c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba82c-115">Return value</span></span>

<span data-ttu-id="ba82c-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba82c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba82c-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba82c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba82c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba82c-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ba82c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba82c-119">Header</span></span></p></td><td><span data-ttu-id="ba82c-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ba82c-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ba82c-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="ba82c-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ba82c-122">**IPeerToPeerEngine**</span><span class="sxs-lookup"><span data-stu-id="ba82c-122">**IPeerToPeerEngine**</span></span>](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
