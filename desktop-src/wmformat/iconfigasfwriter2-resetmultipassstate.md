---
title: Método IConfigAsfWriter2 ResetMultiPassState
description: O método ResetMultiPassState redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Formato de mídia do Windows do método ResetMultiPassState
- Método ResetMultiPassState Windows Media Format, interface IConfigAsfWriter2
- Formato de mídia do Windows de interface IConfigAsfWriter2, método ResetMultiPassState
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366502"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="ab168-106">Método IConfigAsfWriter2:: ResetMultiPassState</span><span class="sxs-lookup"><span data-stu-id="ab168-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="ab168-107">O método **ResetMultiPassState** redefine o filtro quando uma passagem de codificação de pré-processamento é cancelada antes de ser concluída.</span><span class="sxs-lookup"><span data-stu-id="ab168-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab168-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab168-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="ab168-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab168-109">Parameters</span></span>

<span data-ttu-id="ab168-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab168-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab168-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab168-111">Return value</span></span>

<span data-ttu-id="ab168-112">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ab168-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ab168-113">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab168-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ab168-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ab168-114">Return code</span></span>                                                                                         | <span data-ttu-id="ab168-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab168-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="ab168-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab168-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ab168-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ab168-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="ab168-118"><dt>**VFW \_ E \_ não \_ parado**</dt></span><span class="sxs-lookup"><span data-stu-id="ab168-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="ab168-119">O filtro não estava em um estado parado.</span><span class="sxs-lookup"><span data-stu-id="ab168-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab168-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab168-120">Remarks</span></span>

<span data-ttu-id="ab168-121">Esse método deve ser chamado para redefinir o estado interno do filtro sempre que uma passagem de codificação de pré-processamento for cancelada antes que o filtro tenha recebido um evento de **\_ pré-processamento \_ concluído do EC** .</span><span class="sxs-lookup"><span data-stu-id="ab168-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="ab168-122">Não é necessário chamar esse método se a passagem de codificação de pré-processamento for concluída sem erros.</span><span class="sxs-lookup"><span data-stu-id="ab168-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab168-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab168-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab168-124">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab168-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

