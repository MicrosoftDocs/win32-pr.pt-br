---
description: Um retorno de chamada que notifica o host de informações de malha gravados pela solicitação associada.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPipeLineStagesCallback3:: MeshFileReadyCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105775585"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span data-ttu-id="b543c-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>Método IPipeLineStagesCallback3:: MeshFileReadyCallback</span><span class="sxs-lookup"><span data-stu-id="b543c-103"><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback method</span></span>

<span data-ttu-id="b543c-104">Um retorno de chamada que notifica o host de informações de malha gravados pela solicitação associada.</span><span class="sxs-lookup"><span data-stu-id="b543c-104">A callback that notifies the host of Mesh information written by the associated request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b543c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b543c-105">Syntax</span></span>


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a><span data-ttu-id="b543c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b543c-106">Parameters</span></span>

<span data-ttu-id="b543c-107">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="b543c-107">*meshFilename* </span></span>  
<span data-ttu-id="b543c-108">Uma cadeia de caracteres COM que contém o nome do caminho do arquivo onde os dados de malha são gravados.</span><span class="sxs-lookup"><span data-stu-id="b543c-108">A COM string containing the pathname of the file where the mesh data is written.</span></span>

## <a name="return-value"></a><span data-ttu-id="b543c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b543c-109">Return value</span></span>

<span data-ttu-id="b543c-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b543c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b543c-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b543c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b543c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b543c-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b543c-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b543c-113">Header</span></span></p></td><td><span data-ttu-id="b543c-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b543c-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b543c-115"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="b543c-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b543c-116">**IPipeLineStagesCallback3**</span><span class="sxs-lookup"><span data-stu-id="b543c-116">**IPipeLineStagesCallback3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
