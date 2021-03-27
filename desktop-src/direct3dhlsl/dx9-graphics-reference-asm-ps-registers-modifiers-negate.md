---
title: Negação de registro de origem
description: Executa um negação (y x) em todos os componentes de registro.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005408"
---
# <a name="source-register-negate"></a><span data-ttu-id="566ce-103">Negação de registro de origem</span><span class="sxs-lookup"><span data-stu-id="566ce-103">Source Register Negate</span></span>

<span data-ttu-id="566ce-104">Executa um negação (y =-x) em todos os componentes de registro.</span><span class="sxs-lookup"><span data-stu-id="566ce-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="566ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="566ce-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="566ce-106">Registros</span><span class="sxs-lookup"><span data-stu-id="566ce-106">Registers</span></span>

<span data-ttu-id="566ce-107">Registro de origem.</span><span class="sxs-lookup"><span data-stu-id="566ce-107">Source Register.</span></span> <span data-ttu-id="566ce-108">Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="566ce-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="566ce-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="566ce-109">Remarks</span></span>

<span data-ttu-id="566ce-110">O conteúdo do registro não é alterado.</span><span class="sxs-lookup"><span data-stu-id="566ce-110">The contents of the register are not changed.</span></span> <span data-ttu-id="566ce-111">O modificador é aplicado somente aos dados lidos do registro.</span><span class="sxs-lookup"><span data-stu-id="566ce-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="566ce-112">A operação de negação é aplicada a todos os quatro canais de cores (RGBA).</span><span class="sxs-lookup"><span data-stu-id="566ce-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="566ce-113">Essa operação é executada após qualquer outro modificador presente no mesmo argumento.</span><span class="sxs-lookup"><span data-stu-id="566ce-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="566ce-114">Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) para que não possa ser aplicado ao mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="566ce-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="566ce-115">Este modificador é para uso somente com instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="566ce-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="566ce-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="566ce-116">Example</span></span>

<span data-ttu-id="566ce-117">O exemplo a seguir mostra como usar esse modificador.</span><span class="sxs-lookup"><span data-stu-id="566ce-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="566ce-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="566ce-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="566ce-119">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="566ce-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




