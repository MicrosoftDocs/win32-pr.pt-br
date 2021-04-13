---
description: Um retorno de chamada que notifica o host de informações de buffer gravadas em um arquivo pela solicitação assocaited.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IBufferObjectDataCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370328"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="b7b1b-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>Método IBufferObjectDataCallback:: ResultCallback</span><span class="sxs-lookup"><span data-stu-id="b7b1b-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="b7b1b-104">Um retorno de chamada que notifica o host de informações de buffer gravadas em um arquivo pela solicitação assocaited.</span><span class="sxs-lookup"><span data-stu-id="b7b1b-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b1b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7b1b-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="b7b1b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7b1b-106">Parameters</span></span>

<span data-ttu-id="b7b1b-107">Do *arquivo* Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os resultados são gravados.</span><span class="sxs-lookup"><span data-stu-id="b7b1b-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7b1b-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7b1b-108">Return value</span></span>

<span data-ttu-id="b7b1b-109">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b1b-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="b7b1b-110">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7b1b-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b1b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7b1b-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b7b1b-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7b1b-112">Header</span></span></p></td><td><span data-ttu-id="b7b1b-113">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b7b1b-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b7b1b-114"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="b7b1b-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b7b1b-115">**IBufferObjectDataCallback**</span><span class="sxs-lookup"><span data-stu-id="b7b1b-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
