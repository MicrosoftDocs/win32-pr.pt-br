---
title: " Diretiva de erro"
description: Diretiva de pré-processador que produz mensagens de erro de tempo de compilador.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- HLSL de diretiva de erro
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364844"
---
# <a name="error-directive"></a><span data-ttu-id="0bc7a-104">\#Diretiva de erro</span><span class="sxs-lookup"><span data-stu-id="0bc7a-104">\#error Directive</span></span>

<span data-ttu-id="0bc7a-105">Diretiva de pré-processador que produz mensagens de erro de tempo de compilador.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="0bc7a-106">\#*cadeia de caracteres de token de* erro</span><span class="sxs-lookup"><span data-stu-id="0bc7a-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="0bc7a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bc7a-107">Parameters</span></span>



| <span data-ttu-id="0bc7a-108">Item</span><span class="sxs-lookup"><span data-stu-id="0bc7a-108">Item</span></span>                                                                                    | <span data-ttu-id="0bc7a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bc7a-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc7a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Cadeia de caracteres de token*</span><span class="sxs-lookup"><span data-stu-id="0bc7a-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="0bc7a-111">Mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-111">Error message.</span></span> <span data-ttu-id="0bc7a-112">Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="0bc7a-113">A cadeia de caracteres do token está sujeita à expansão de macro.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0bc7a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bc7a-114">Remarks</span></span>

<span data-ttu-id="0bc7a-115">\#as diretivas de erro são mais úteis para detectar inconsistências de programador e violação de restrições durante o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="0bc7a-116">Quando uma \# diretiva de erro é encontrada, a compilação é encerrada.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="0bc7a-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bc7a-117">Examples</span></span>

<span data-ttu-id="0bc7a-118">O exemplo a seguir demonstra o processamento de erros durante o pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="0bc7a-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="0bc7a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bc7a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc7a-120">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc7a-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





