---
description: Recupera a versão do software para este fluxo.
ms.assetid: f54153df-5593-4784-acc5-3e0dcef424b5
title: Método CPersistStream. GetSoftwareVersion (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSoftwareVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0954e9a113342217dd389c64ec4fc6c04a6f767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760758"
---
# <a name="cpersiststreamgetsoftwareversion-method"></a><span data-ttu-id="65b80-103">Método CPersistStream. GetSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="65b80-103">CPersistStream.GetSoftwareVersion method</span></span>

<span data-ttu-id="65b80-104">Recupera a versão do software para este fluxo.</span><span class="sxs-lookup"><span data-stu-id="65b80-104">Retrieves the software version for this stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b80-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65b80-105">Syntax</span></span>


```C++
virtual DWORD GetSoftwareVersion();
```



## <a name="parameters"></a><span data-ttu-id="65b80-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65b80-106">Parameters</span></span>

<span data-ttu-id="65b80-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="65b80-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65b80-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65b80-108">Return value</span></span>

<span data-ttu-id="65b80-109">Retorna um **DWORD** que contém o número de versão.</span><span class="sxs-lookup"><span data-stu-id="65b80-109">Returns a **DWORD** containing the version number.</span></span> <span data-ttu-id="65b80-110">Cada vez que o formato do fluxo é alterado, essa função deve ser alterada para retornar um número maior do que antes.</span><span class="sxs-lookup"><span data-stu-id="65b80-110">Each time the format of the stream is changed, this function should be altered to return a larger number than before.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b80-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65b80-111">Requirements</span></span>



| <span data-ttu-id="65b80-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b80-112">Requirement</span></span> | <span data-ttu-id="65b80-113">Valor</span><span class="sxs-lookup"><span data-stu-id="65b80-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b80-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65b80-114">Header</span></span><br/>  | <dl> <span data-ttu-id="65b80-115"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65b80-115"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65b80-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65b80-116">Library</span></span><br/> | <dl> <span data-ttu-id="65b80-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="65b80-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b80-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="65b80-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b80-119">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="65b80-119">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




