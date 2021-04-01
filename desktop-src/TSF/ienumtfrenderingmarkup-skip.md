---
title: Método IEnumTfRenderingMarkup Skip
description: O método IEnumTfRenderingMarkup Skip Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Ignorar a estrutura de serviços de texto de método
- Ignorar método texto estrutura de serviços, interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, método Skip
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638459"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="cbab2-106">Método IEnumTfRenderingMarkup:: Skip</span><span class="sxs-lookup"><span data-stu-id="cbab2-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="cbab2-107">O método **IEnumTfRenderingMarkup:: Skip** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="cbab2-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbab2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbab2-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="cbab2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbab2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbab2-110">*ulCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cbab2-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbab2-111">\[in \] especifica o número de elementos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="cbab2-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbab2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbab2-112">Return value</span></span>

<span data-ttu-id="cbab2-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="cbab2-113">This method can return one of these values.</span></span>



| <span data-ttu-id="cbab2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cbab2-114">Value</span></span>                                                                                   | <span data-ttu-id="cbab2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cbab2-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbab2-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cbab2-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cbab2-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cbab2-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="cbab2-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="cbab2-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cbab2-119">O método atingiu o final da enumeração antes que o número especificado de elementos pudesse ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="cbab2-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cbab2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbab2-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbab2-121">Esse método não está atualmente nos arquivos de cabeçalho públicos.</span><span class="sxs-lookup"><span data-stu-id="cbab2-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="cbab2-122">Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.</span><span class="sxs-lookup"><span data-stu-id="cbab2-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





