---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Método IMpeg2PsiParser:: GetCountOfPrograms'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825872"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="df887-104">Método IMpeg2PsiParser:: GetCountOfPrograms</span><span class="sxs-lookup"><span data-stu-id="df887-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="df887-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="df887-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="df887-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="df887-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="df887-107">O `GetCountOfPrograms` método recupera o número de programas no fluxo de transporte.</span><span class="sxs-lookup"><span data-stu-id="df887-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="df887-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df887-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="df887-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df887-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df887-110">*pNumOfPrograms* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df887-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df887-111">Ponteiro para uma variável que recebe o número de programas.</span><span class="sxs-lookup"><span data-stu-id="df887-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df887-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df887-112">Return value</span></span>

<span data-ttu-id="df887-113">O método retorna um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="df887-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="df887-114">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="df887-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="df887-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="df887-115">Return code</span></span>                                                                          | <span data-ttu-id="df887-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="df887-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="df887-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df887-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df887-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="df887-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="df887-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="df887-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df887-120">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="df887-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="df887-121">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="df887-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




