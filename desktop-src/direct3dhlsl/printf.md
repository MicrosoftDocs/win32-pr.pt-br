---
title: printf - função
description: Envia uma mensagem de sombreador personalizado para a fila de informações.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- função printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916810"
---
# <a name="printf-function"></a><span data-ttu-id="eb407-104">printf - função</span><span class="sxs-lookup"><span data-stu-id="eb407-104">printf function</span></span>

<span data-ttu-id="eb407-105">Envia uma mensagem de sombreador personalizado para a fila de informações.</span><span class="sxs-lookup"><span data-stu-id="eb407-105">Submits a custom shader message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb407-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb407-106">Syntax</span></span>

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="eb407-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb407-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb407-108">*format*</span><span class="sxs-lookup"><span data-stu-id="eb407-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="eb407-109">A cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="eb407-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="eb407-110">*argumento...*</span><span class="sxs-lookup"><span data-stu-id="eb407-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="eb407-111">Argumentos opcionais.</span><span class="sxs-lookup"><span data-stu-id="eb407-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb407-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb407-112">Return value</span></span>

<span data-ttu-id="eb407-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eb407-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb407-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb407-114">Remarks</span></span>

<span data-ttu-id="eb407-115">Esta operação não faz nada em dispositivos que não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="eb407-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="eb407-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="eb407-116">Minimum Shader Model</span></span>

<span data-ttu-id="eb407-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eb407-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eb407-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="eb407-118">Shader Model</span></span>                                                        | <span data-ttu-id="eb407-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="eb407-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="eb407-120">Shader Model 4 (DirectX HLSL) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="eb407-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eb407-121">sim</span><span class="sxs-lookup"><span data-stu-id="eb407-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="eb407-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb407-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb407-123">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="eb407-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




