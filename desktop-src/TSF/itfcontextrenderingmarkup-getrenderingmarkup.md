---
title: Método ITfContextRenderingMarkup GetRenderingMarkup
description: O método ITfContextRenderingMarkup GetRenderingMarkup recupera um enumerador das marcações de renderização para o intervalo especificado.
ms.assetid: fe060eab-8a6b-4eb7-9c7f-353b887657d8
keywords:
- Estrutura de serviços de texto do método GetRenderingMarkup
- Método GetRenderingMarkup de estrutura de serviços de texto, interface ITfContextRenderingMarkup
- Estrutura de serviços de texto da interface ITfContextRenderingMarkup, método GetRenderingMarkup
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup.GetRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f3ccfb97af6a6657c33982359640a2a924cad2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641413"
---
# <a name="itfcontextrenderingmarkupgetrenderingmarkup-method"></a><span data-ttu-id="5ccc3-106">Método ITfContextRenderingMarkup:: GetRenderingMarkup</span><span class="sxs-lookup"><span data-stu-id="5ccc3-106">ITfContextRenderingMarkup::GetRenderingMarkup method</span></span>

<span data-ttu-id="5ccc3-107">O método **ITfContextRenderingMarkup:: GetRenderingMarkup** recupera um enumerador das marcações de renderização para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-107">The **ITfContextRenderingMarkup::GetRenderingMarkup** method retrieves an enumerator of the rendering markups for the given range.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccc3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ccc3-108">Syntax</span></span>


```C++
HRESULT GetRenderingMarkup(
  [in]  TfEditCookie           ec,
  [in]  DWORD                  dwFlags,
  [in]  ITfRange               *pRangeCover,
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5ccc3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ccc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ccc3-110">*EC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ccc3-110">*ec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc3-111">\[em \] um cookie de edição somente leitura para acessar o contexto.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-111">\[in\] A read only edit cookie to access the context.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc3-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ccc3-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc3-113">\[Em\]</span><span class="sxs-lookup"><span data-stu-id="5ccc3-113">\[in\]</span></span>



| <span data-ttu-id="5ccc3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5ccc3-114">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="5ccc3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5ccc3-115">Meaning</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="TF_GRM_INCLUDE_PROPERTY"></span><span id="tf_grm_include_property"></span><dl> <span data-ttu-id="5ccc3-116"><dt>**Propriedade de inclusão de TF \_ GRM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc3-116"><dt>**TF\_GRM\_INCLUDE\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="5ccc3-117">Se esse bit for 1, o enumerador incluirá a \_ propriedade de atributo de prop de GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="5ccc3-117">If this bit is 1, the enumerator will include the GUID\_PROP\_ATTRIBUTE property.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5ccc3-118">*pRangeCover* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ccc3-118">*pRangeCover* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc3-119">\[em \] um ponteiro para uma interface [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) do intervalo para enumerar as marcações de renderização.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-119">\[in\] A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface of the range to enumerate the rendering markups.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc3-120">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ccc3-120">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc3-121">\[\]um ponteiro para recuperar o ponteiro de interface [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) .</span><span class="sxs-lookup"><span data-stu-id="5ccc3-121">\[out\] A pointer to retrieve [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ccc3-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ccc3-122">Return value</span></span>

<span data-ttu-id="5ccc3-123">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-123">This method can return one of these values.</span></span>



| <span data-ttu-id="5ccc3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5ccc3-124">Value</span></span>                                                                                | <span data-ttu-id="5ccc3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ccc3-125">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5ccc3-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc3-126"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5ccc3-127">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-127">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ccc3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ccc3-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ccc3-129">Esse método não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-129">This method is not currently in the public header files.</span></span> <span data-ttu-id="5ccc3-130">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="5ccc3-130">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

