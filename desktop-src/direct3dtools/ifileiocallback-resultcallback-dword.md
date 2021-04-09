---
description: Uma função de retorno de chamada usada para notificar o host de erros durante a captura ou reprodução.
MS-HAID: vspixengine.IFileIOCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IFileIOCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E4418A63-47C6-4F12-94FA-0F1B5465FE84
api_name:
- IFileIOCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 751c4d0b57165e148002218ae2151aaba69e48f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087639"
---
# <a name="span-idvspixengineifileiocallback_resultcallback_dwordspanifileiocallbackresultcallback-method"></a><span data-ttu-id="cf497-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>Método IFileIOCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="cf497-103"><span id="vspixengine.ifileiocallback_resultcallback_dword"></span>IFileIOCallback::ResultCallback method</span></span>

<span data-ttu-id="cf497-104">Uma função de retorno de chamada usada para notificar o host de erros durante a captura ou reprodução.</span><span class="sxs-lookup"><span data-stu-id="cf497-104">A callback function used to notify the host of errors while during capture or playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf497-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf497-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD resultState
);
```

## <a name="parameters"></a><span data-ttu-id="cf497-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf497-106">Parameters</span></span>

<span data-ttu-id="cf497-107">*resultadostate* </span><span class="sxs-lookup"><span data-stu-id="cf497-107">*resultState* </span></span>  
<span data-ttu-id="cf497-108">Indica o tipo de erro encontrado.</span><span class="sxs-lookup"><span data-stu-id="cf497-108">Indicates the kind of error encountered.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf497-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf497-109">Return value</span></span>

<span data-ttu-id="cf497-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cf497-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf497-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf497-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf497-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf497-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cf497-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf497-113">Header</span></span></p></td><td><span data-ttu-id="cf497-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cf497-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cf497-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="cf497-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cf497-116">**IFileIOCallback**</span><span class="sxs-lookup"><span data-stu-id="cf497-116">**IFileIOCallback**</span></span>](/windows/desktop/direct3dtools/ifileiocallback)

 

 
