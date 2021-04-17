---
description: Indica se a cadeia de caracteres reconhecida deste IContextNode veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Método IContextNode:: IsStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770549"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="f5295-103">Método IContextNode:: IsStringSupported</span><span class="sxs-lookup"><span data-stu-id="f5295-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="f5295-104">Indica se a cadeia de caracteres reconhecida deste [**IContextNode**](icontextnode.md) veio do dicionário do sistema, do dicionário do usuário ou da lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="f5295-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5295-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5295-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="f5295-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5295-107">*pfIsSupported* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f5295-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f5295-108">**Variante \_ TRUE** se o valor de cadeia de caracteres reconhecido desse [**IContextNode**](icontextnode.md) for suportado pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) com quaisquer nós de dica correspondentes aplicados; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f5295-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5295-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5295-109">Return value</span></span>

<span data-ttu-id="f5295-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5295-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5295-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5295-111">Requirements</span></span>



| <span data-ttu-id="f5295-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5295-112">Requirement</span></span> | <span data-ttu-id="f5295-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f5295-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5295-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5295-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f5295-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5295-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5295-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5295-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f5295-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5295-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5295-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5295-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5295-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5295-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5295-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f5295-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5295-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5295-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5295-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5295-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5295-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f5295-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




