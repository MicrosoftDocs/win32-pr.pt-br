---
description: Solicitações para obter informações sobre quais colunas (campos) esse tipo de solicitação de tabela de objeto dá suporte.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IObjectTableRequest:: RequestSupportedColumnsAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500724"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="9b1c6-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Método IObjectTableRequest:: RequestSupportedColumnsAsync</span><span class="sxs-lookup"><span data-stu-id="9b1c6-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="9b1c6-104">Solicitações para obter informações sobre quais colunas (campos) esse tipo de solicitação de tabela de objeto dá suporte.</span><span class="sxs-lookup"><span data-stu-id="9b1c6-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b1c6-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="9b1c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b1c6-106">Parameters</span></span>

<span data-ttu-id="9b1c6-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="9b1c6-107">*requestCallback* </span></span>  
<span data-ttu-id="9b1c6-108">O endereço do retorno de chamada usado para notificar o host dos resultados.</span><span class="sxs-lookup"><span data-stu-id="9b1c6-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="9b1c6-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="9b1c6-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="9b1c6-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="9b1c6-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="9b1c6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b1c6-111">Return value</span></span>

<span data-ttu-id="9b1c6-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9b1c6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9b1c6-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9b1c6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b1c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b1c6-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9b1c6-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9b1c6-115">Header</span></span></p></td><td><span data-ttu-id="9b1c6-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9b1c6-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9b1c6-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="9b1c6-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9b1c6-118">**IObjectTableRequest**</span><span class="sxs-lookup"><span data-stu-id="9b1c6-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
