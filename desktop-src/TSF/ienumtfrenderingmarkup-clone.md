---
title: Método Clone IEnumTfRenderingMarkup
description: O método clone IEnumTfRenderingMarkup cria uma cópia do objeto enumerador.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Estrutura de serviços de texto de método de clonagem
- Método clone de serviços de texto text Framework, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, método clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105796339"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="a3668-106">Método IEnumTfRenderingMarkup:: clone</span><span class="sxs-lookup"><span data-stu-id="a3668-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="a3668-107">O método **IEnumTfRenderingMarkup:: clone** cria uma cópia do objeto enumerador.</span><span class="sxs-lookup"><span data-stu-id="a3668-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3668-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3668-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="a3668-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3668-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3668-110">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3668-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3668-111">\[\]um ponteiro para uma interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="a3668-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3668-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3668-112">Return value</span></span>

<span data-ttu-id="a3668-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a3668-113">This method can return one of these values.</span></span>



| <span data-ttu-id="a3668-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a3668-114">Value</span></span>                                                                                        | <span data-ttu-id="a3668-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3668-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a3668-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3668-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a3668-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a3668-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="a3668-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a3668-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="a3668-119">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a3668-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="a3668-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a3668-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a3668-121">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="a3668-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3668-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3668-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3668-123">Esse método não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="a3668-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="a3668-124">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="a3668-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

