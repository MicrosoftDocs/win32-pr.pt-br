---
title: função errorf
description: Envia uma mensagem de erro para a fila de informações.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- HLSL da função errorf
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006406"
---
# <a name="errorf-function"></a><span data-ttu-id="298ed-104">função errorf</span><span class="sxs-lookup"><span data-stu-id="298ed-104">errorf function</span></span>

<span data-ttu-id="298ed-105">Envia uma mensagem de erro para a fila de informações.</span><span class="sxs-lookup"><span data-stu-id="298ed-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="298ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="298ed-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="298ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="298ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="298ed-108">*format*</span><span class="sxs-lookup"><span data-stu-id="298ed-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="298ed-109">A cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="298ed-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="298ed-110">*argumento...*</span><span class="sxs-lookup"><span data-stu-id="298ed-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="298ed-111">Argumentos opcionais.</span><span class="sxs-lookup"><span data-stu-id="298ed-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="298ed-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="298ed-112">Return value</span></span>

<span data-ttu-id="298ed-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="298ed-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="298ed-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="298ed-114">Remarks</span></span>

<span data-ttu-id="298ed-115">Esta operação não faz nada em dispositivos que não dão suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="298ed-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="298ed-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="298ed-116">Minimum Shader Model</span></span>

<span data-ttu-id="298ed-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="298ed-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="298ed-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="298ed-118">Shader Model</span></span>                                                        | <span data-ttu-id="298ed-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="298ed-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="298ed-120">Shader Model 4 (DirectX HLSL) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="298ed-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="298ed-121">sim</span><span class="sxs-lookup"><span data-stu-id="298ed-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="298ed-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="298ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298ed-123">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="298ed-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




