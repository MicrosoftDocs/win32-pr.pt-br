---
title: " Diretiva pragma"
description: Diretiva de pré-processador que fornece recursos específicos do computador ou do sistema operacional, mantendo a compatibilidade geral com as linguagens C e C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- HLSL de diretiva de pragma
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006542"
---
# <a name="pragma-directive"></a><span data-ttu-id="33785-104">\#Diretiva pragma</span><span class="sxs-lookup"><span data-stu-id="33785-104">\#pragma Directive</span></span>

<span data-ttu-id="33785-105">Diretiva de pré-processador que fornece recursos específicos do computador ou do sistema operacional, mantendo a compatibilidade geral com as linguagens C e C++.</span><span class="sxs-lookup"><span data-stu-id="33785-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="33785-106">\#pragma *token-cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="33785-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="33785-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33785-107">Parameters</span></span>



| <span data-ttu-id="33785-108">Item</span><span class="sxs-lookup"><span data-stu-id="33785-108">Item</span></span>                                                                                    | <span data-ttu-id="33785-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="33785-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33785-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Cadeia de caracteres de token*</span><span class="sxs-lookup"><span data-stu-id="33785-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="33785-111">Série de caracteres que fornece instruções e argumentos específicos do compilador.</span><span class="sxs-lookup"><span data-stu-id="33785-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="33785-112">Este parâmetro está sujeito à expansão de macro.</span><span class="sxs-lookup"><span data-stu-id="33785-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="33785-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="33785-113">Remarks</span></span>

<span data-ttu-id="33785-114">Se o compilador encontrar um pragma não reconhecido, ele emitirá um aviso, mas a compilação continuará.</span><span class="sxs-lookup"><span data-stu-id="33785-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="33785-115">O compilador HLSL reconhece os seguintes pragmas:</span><span class="sxs-lookup"><span data-stu-id="33785-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="33785-116">particular</span><span class="sxs-lookup"><span data-stu-id="33785-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="33785-117">message</span><span class="sxs-lookup"><span data-stu-id="33785-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="33785-118">matriz de pacote \_</span><span class="sxs-lookup"><span data-stu-id="33785-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="33785-119">warning</span><span class="sxs-lookup"><span data-stu-id="33785-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="33785-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="33785-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33785-121">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33785-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





