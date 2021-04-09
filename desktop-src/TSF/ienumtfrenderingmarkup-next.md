---
title: Método Next IEnumTfRenderingMarkup
description: O método Next IEnumTfRenderingMarkup Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Próxima método de estrutura de serviços de texto
- Próxima método de estrutura de serviços de texto, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, próximo método
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007797"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="601bf-106">Método IEnumTfRenderingMarkup:: Next</span><span class="sxs-lookup"><span data-stu-id="601bf-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="601bf-107">O método **IEnumTfRenderingMarkup:: Next** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="601bf-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="601bf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="601bf-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="601bf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="601bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601bf-110">*ulCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="601bf-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601bf-111">\[out \] especifica o número de elementos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="601bf-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="601bf-112">*ppElement* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="601bf-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601bf-113">\[ponteiro de saída \] para uma matriz de estruturas de [ \_ RENDERINGMARKUP de TF](/windows/desktop/TSF/tf-renderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="601bf-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="601bf-114">Essa matriz deve ter pelo menos elementos *ulCount* de tamanho.</span><span class="sxs-lookup"><span data-stu-id="601bf-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="601bf-115">*pcFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="601bf-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601bf-116">\[\]ponteiro de saída para um valor ULONG que recebe o número de elementos realmente obtidos.</span><span class="sxs-lookup"><span data-stu-id="601bf-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="601bf-117">Esse valor pode ser menor que o número de itens solicitados.</span><span class="sxs-lookup"><span data-stu-id="601bf-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="601bf-118">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="601bf-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601bf-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="601bf-119">Return value</span></span>

<span data-ttu-id="601bf-120">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="601bf-120">This method can return one of these values.</span></span>



| <span data-ttu-id="601bf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="601bf-121">Value</span></span>                                                                                        | <span data-ttu-id="601bf-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="601bf-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="601bf-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="601bf-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="601bf-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="601bf-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="601bf-125"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="601bf-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="601bf-126">O método atingiu o final da enumeração antes que o número especificado de elementos pudesse ser obtido.</span><span class="sxs-lookup"><span data-stu-id="601bf-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="601bf-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="601bf-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="601bf-128">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="601bf-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="601bf-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="601bf-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="601bf-130">Esse método não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="601bf-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="601bf-131">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="601bf-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

