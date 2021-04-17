---
description: A função LoadOLEAut32 carrega a biblioteca de vínculo dinâmico de automação (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: Função LoadOLEAut32 (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812976"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="7e22b-103">Função LoadOLEAut32</span><span class="sxs-lookup"><span data-stu-id="7e22b-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="7e22b-104">A função **LoadOLEAut32** carrega a biblioteca de vínculo dinâmico de automação (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="7e22b-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e22b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e22b-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="7e22b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e22b-106">Parameters</span></span>

<span data-ttu-id="7e22b-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7e22b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e22b-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7e22b-108">Return value</span></span>

<span data-ttu-id="7e22b-109">Retorna um identificador para uma instância de DLL de automação.</span><span class="sxs-lookup"><span data-stu-id="7e22b-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e22b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e22b-110">Remarks</span></span>

<span data-ttu-id="7e22b-111">Quando o destruidor [**CBaseObject**](cbaseobject.md) destrói o objeto que carregou OleAut32.dll, ele descarregará a biblioteca se ainda estiver carregada.</span><span class="sxs-lookup"><span data-stu-id="7e22b-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e22b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e22b-112">Requirements</span></span>



| <span data-ttu-id="7e22b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e22b-113">Requirement</span></span> | <span data-ttu-id="7e22b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7e22b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e22b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e22b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7e22b-116"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e22b-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7e22b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e22b-117">Library</span></span><br/> | <dl> <span data-ttu-id="7e22b-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7e22b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e22b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e22b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e22b-120">**Funções auxiliares COM**</span><span class="sxs-lookup"><span data-stu-id="7e22b-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




