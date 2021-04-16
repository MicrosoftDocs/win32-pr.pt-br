---
description: Encerra o experiement e conclui o log de gráficos.
MS-HAID: vspixengine.IPixEngine2\_EndExperiment\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Método IPixEngine2:: endexperimento'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0260F337-B279-4FE6-92F3-FCF70C2B8980
api_name:
- IPixEngine2.EndExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2638c75269f93e50fd1f9e4b6938b123cbd01e60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500422"
---
# <a name="span-idvspixengineipixengine2_endexperiment_bstr_ifileiocallback_ptrspanipixengine2endexperiment-method"></a><span data-ttu-id="eaf49-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>Método IPixEngine2:: endexperimento</span><span class="sxs-lookup"><span data-stu-id="eaf49-103"><span id="vspixengine.ipixengine2_endexperiment_bstr_ifileiocallback_ptr"></span>IPixEngine2::EndExperiment method</span></span>

<span data-ttu-id="eaf49-104">Encerra o experiement e conclui o log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="eaf49-104">Ends the experiement and completes the graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf49-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaf49-105">Syntax</span></span>


```C++
HRESULT EndExperiment(
   BSTR              logFile,
   IFileIOCallback * pCallback
);
```

## <a name="parameters"></a><span data-ttu-id="eaf49-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaf49-106">Parameters</span></span>

<span data-ttu-id="eaf49-107">*Restaura* </span><span class="sxs-lookup"><span data-stu-id="eaf49-107">*logFile* </span></span>  
<span data-ttu-id="eaf49-108">Uma cadeia de caracteres COM que contém o nome do log de gráficos.</span><span class="sxs-lookup"><span data-stu-id="eaf49-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="eaf49-109">*pCallback* </span><span class="sxs-lookup"><span data-stu-id="eaf49-109">*pCallback* </span></span>  
<span data-ttu-id="eaf49-110">O endereço de um retorno de chamada usado para indicar que o experiement foi finalizado.</span><span class="sxs-lookup"><span data-stu-id="eaf49-110">The address of a callback used to indicate that the experiement is ended.</span></span>

## <a name="return-value"></a><span data-ttu-id="eaf49-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaf49-111">Return value</span></span>

<span data-ttu-id="eaf49-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eaf49-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eaf49-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eaf49-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf49-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaf49-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eaf49-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eaf49-115">Header</span></span></p></td><td><span data-ttu-id="eaf49-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eaf49-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eaf49-117"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="eaf49-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eaf49-118">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="eaf49-118">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
