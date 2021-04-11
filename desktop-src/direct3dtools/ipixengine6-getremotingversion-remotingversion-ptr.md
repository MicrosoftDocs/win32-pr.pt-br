---
description: Obtém a versão de comunicação remota do mecanismo.
MS-HAID: vspixengine.IPixEngine6\_GetRemotingVersion\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine6:: GetRemotingVersion'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 065FC3A7-ECFB-4551-B4B0-CA0E6B8676F8
api_name:
- IPixEngine6.GetRemotingVersion
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85230a71d9c0f2dd437ec25af3eb6c660f032586
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009992"
---
# <a name="span-idvspixengineipixengine6_getremotingversion_remotingversion_ptrspanipixengine6getremotingversion-method"></a><span data-ttu-id="8ddb7-103"><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>Método IPixEngine6:: GetRemotingVersion</span><span class="sxs-lookup"><span data-stu-id="8ddb7-103"><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>IPixEngine6::GetRemotingVersion method</span></span>

<span data-ttu-id="8ddb7-104">Obtém a versão de comunicação remota do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="8ddb7-104">Gets the remoting version of the engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ddb7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ddb7-105">Syntax</span></span>


```C++
HRESULT GetRemotingVersion(
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a><span data-ttu-id="8ddb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ddb7-106">Parameters</span></span>

<span data-ttu-id="8ddb7-107">*pRemoteVersion* </span><span class="sxs-lookup"><span data-stu-id="8ddb7-107">*pRemoteVersion* </span></span>  
<span data-ttu-id="8ddb7-108">A versão de comunicação remota do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="8ddb7-108">The remoting version of the engine.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ddb7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ddb7-109">Return value</span></span>

<span data-ttu-id="8ddb7-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8ddb7-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8ddb7-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ddb7-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ddb7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ddb7-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8ddb7-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ddb7-113">Header</span></span></p></td><td><span data-ttu-id="8ddb7-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8ddb7-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8ddb7-115"><span id="see_also"></span>Consulte também</span><span class="sxs-lookup"><span data-stu-id="8ddb7-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8ddb7-116">**IPixEngine6**</span><span class="sxs-lookup"><span data-stu-id="8ddb7-116">**IPixEngine6**</span></span>](/windows/desktop/direct3dtools/ipixengine6)

 

 
