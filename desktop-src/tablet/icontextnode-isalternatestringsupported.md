---
description: Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Método IContextNode:: IsAlternateStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783215"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="b2474-103">Método IContextNode:: IsAlternateStringSupported</span><span class="sxs-lookup"><span data-stu-id="b2474-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="b2474-104">Indica se a cadeia de caracteres reconhecida especificada veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="b2474-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="b2474-105">Qualquer dado de restrição, como listas de palavras, guias ou factores, em qualquer nó de dica correspondente será usado para determinar se há suporte para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b2474-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2474-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2474-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="b2474-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2474-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2474-108">*bstrAlternateString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2474-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2474-109">Cadeia de caracteres reconhecida para verificar.</span><span class="sxs-lookup"><span data-stu-id="b2474-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="b2474-110">*pfIsSupported* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b2474-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2474-111">**Variante \_ TRUE** se a cadeia de caracteres especificada for suportada pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) com quaisquer nós de dica correspondentes aplicados; **Variante \_ FALSE** se não houver suporte.</span><span class="sxs-lookup"><span data-stu-id="b2474-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2474-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2474-112">Return value</span></span>

<span data-ttu-id="b2474-113">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b2474-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2474-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2474-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b2474-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2474-115">Requirements</span></span>



| <span data-ttu-id="b2474-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2474-116">Requirement</span></span> | <span data-ttu-id="b2474-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b2474-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2474-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2474-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2474-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b2474-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b2474-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2474-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2474-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b2474-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b2474-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2474-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2474-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b2474-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b2474-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b2474-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2474-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2474-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b2474-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2474-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2474-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b2474-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




