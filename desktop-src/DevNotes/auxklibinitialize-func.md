---
description: Inicializa a \_ biblioteca Klib aux.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Função AuxKlibInitialize (aux \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747682"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="2de78-103">Função AuxKlibInitialize</span><span class="sxs-lookup"><span data-stu-id="2de78-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="2de78-104">Inicializa a \_ biblioteca Klib aux.</span><span class="sxs-lookup"><span data-stu-id="2de78-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="2de78-105">Essa função deve ser chamada antes que qualquer outra função na biblioteca possa ser chamada.</span><span class="sxs-lookup"><span data-stu-id="2de78-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de78-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de78-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="2de78-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2de78-107">Parameters</span></span>

<span data-ttu-id="2de78-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2de78-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2de78-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2de78-109">Return value</span></span>

<span data-ttu-id="2de78-110">Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.</span><span class="sxs-lookup"><span data-stu-id="2de78-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="2de78-111">Se a função falhar, o valor de retorno poderá ser um dos códigos de status definidos em Ntstatus. h, que está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="2de78-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de78-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2de78-112">Remarks</span></span>

<span data-ttu-id="2de78-113">A biblioteca de objetos que implementa essa API pode ser baixada [aqui](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="2de78-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="2de78-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de78-114">Requirements</span></span>



| <span data-ttu-id="2de78-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de78-115">Requirement</span></span> | <span data-ttu-id="2de78-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2de78-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de78-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2de78-117">Redistributable</span></span><br/> | <span data-ttu-id="2de78-118">Biblioteca de API auxiliar do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2de78-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="2de78-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2de78-119">Header</span></span><br/>          | <dl> <span data-ttu-id="2de78-120"><dt>\_Klib aux. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de78-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="2de78-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2de78-121">Library</span></span><br/>         | <dl> <span data-ttu-id="2de78-122"><dt>\_Klib. lib do aux</dt></span><span class="sxs-lookup"><span data-stu-id="2de78-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de78-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de78-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de78-124">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="2de78-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




