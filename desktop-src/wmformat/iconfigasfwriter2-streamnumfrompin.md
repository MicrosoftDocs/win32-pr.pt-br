---
title: Método IConfigAsfWriter2 StreamNumFromPin
description: O método StreamNumFromPin recupera o número de fluxo associado ao PIN de entrada especificado.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Formato de mídia do Windows do método StreamNumFromPin
- Método StreamNumFromPin Windows Media Format, interface IConfigAsfWriter2
- Formato de mídia do Windows de interface IConfigAsfWriter2, método StreamNumFromPin
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366150"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a><span data-ttu-id="5eb4f-106">Método IConfigAsfWriter2:: StreamNumFromPin</span><span class="sxs-lookup"><span data-stu-id="5eb4f-106">IConfigAsfWriter2::StreamNumFromPin method</span></span>

<span data-ttu-id="5eb4f-107">O método **StreamNumFromPin** recupera o número de fluxo associado ao PIN de entrada especificado.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-107">The **StreamNumFromPin** method retrieves the stream number associated with the specified input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb4f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5eb4f-108">Syntax</span></span>


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a><span data-ttu-id="5eb4f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eb4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb4f-110">*pPin* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5eb4f-110">*pPin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb4f-111">Ponteiro para a interface **IPin** no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-111">Pointer to the **IPin** interface on the input pin.</span></span>

</dd> <dt>

<span data-ttu-id="5eb4f-112">*pwStreamNum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5eb4f-112">*pwStreamNum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5eb4f-113">Ponteiro que recebe o número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-113">Pointer that receives the stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb4f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5eb4f-114">Return value</span></span>

<span data-ttu-id="5eb4f-115">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5eb4f-116">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5eb4f-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb4f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5eb4f-117">Remarks</span></span>

<span data-ttu-id="5eb4f-118">Às vezes, talvez seja necessário usar as interfaces do Windows Media Format SDK diretamente para manipular um fluxo antes de executar um gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-118">Sometimes you may need to use the Windows Media Format SDK interfaces directly to manipulate a stream before running a filter graph.</span></span> <span data-ttu-id="5eb4f-119">Como você não pode pressupor que um número de fluxo de ASF seja o mesmo que o número de PIN do DirectShow, esse método é fornecido.</span><span class="sxs-lookup"><span data-stu-id="5eb4f-119">Because you cannot assume that an ASF stream number is the same as the DirectShow pin number, this method is provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb4f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eb4f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="5eb4f-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5eb4f-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

 