---
description: Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Ponteiro de função LPFNInitRoutine (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754756"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="4e6a3-103">Ponteiro de função LPFNInitRoutine</span><span class="sxs-lookup"><span data-stu-id="4e6a3-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="4e6a3-104">Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="4e6a3-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e6a3-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="4e6a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e6a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6a3-107">*bLoading*</span><span class="sxs-lookup"><span data-stu-id="4e6a3-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="4e6a3-108">**True** quando a DLL for carregada, **false** quando a DLL for descarregada.</span><span class="sxs-lookup"><span data-stu-id="4e6a3-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4e6a3-109">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="4e6a3-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="4e6a3-110">Ponteiro para o CLISD do objeto, especificado na variável de membro [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="4e6a3-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6a3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e6a3-111">Return value</span></span>

<span data-ttu-id="4e6a3-112">Esse ponteiro de função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4e6a3-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6a3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e6a3-113">Requirements</span></span>



| <span data-ttu-id="4e6a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e6a3-114">Requirement</span></span> | <span data-ttu-id="4e6a3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4e6a3-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6a3-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e6a3-116">Header</span></span><br/> | <dl> <span data-ttu-id="4e6a3-117"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e6a3-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e6a3-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e6a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6a3-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="4e6a3-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




