---
description: A função DbgSetModuleLevel define o nível de log para um ou mais tipos de mensagem. Ignorado em compilações de varejo.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Função DbgSetModuleLevel (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750646"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="46c4e-104">Função DbgSetModuleLevel</span><span class="sxs-lookup"><span data-stu-id="46c4e-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="46c4e-105">A função **DbgSetModuleLevel** define o nível de log para um ou mais tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="46c4e-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="46c4e-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="46c4e-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c4e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46c4e-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="46c4e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46c4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c4e-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="46c4e-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="46c4e-110">Combinação de bits de um ou mais tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="46c4e-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="46c4e-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="46c4e-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="46c4e-112">Nível de log para os tipos de mensagem especificados.</span><span class="sxs-lookup"><span data-stu-id="46c4e-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c4e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46c4e-113">Return value</span></span>

<span data-ttu-id="46c4e-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="46c4e-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46c4e-115">Requirements</span></span>



| <span data-ttu-id="46c4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c4e-116">Requirement</span></span> | <span data-ttu-id="46c4e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="46c4e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c4e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46c4e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="46c4e-119"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46c4e-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46c4e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46c4e-120">Library</span></span><br/> | <dl> <span data-ttu-id="46c4e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="46c4e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46c4e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="46c4e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c4e-123">Funções de saída de depuração</span><span class="sxs-lookup"><span data-stu-id="46c4e-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




