---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Método IMpeg2PsiParser:: GetRecordProgramNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768598"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="0a6c2-104">Método IMpeg2PsiParser:: GetRecordProgramNumber</span><span class="sxs-lookup"><span data-stu-id="0a6c2-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="0a6c2-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="0a6c2-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="0a6c2-107">O `GetRecordProgramNumber` método recupera o número do programa para um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6c2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a6c2-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="0a6c2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a6c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6c2-110">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a6c2-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6c2-111">Especifica a entrada no PAT que define o programa, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="0a6c2-112">*pwVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a6c2-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6c2-113">Ponteiro para uma variável que recebe o \_ campo de número do programa do Pat.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6c2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a6c2-114">Return value</span></span>

<span data-ttu-id="0a6c2-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a6c2-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="0a6c2-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="0a6c2-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0a6c2-117">Return code</span></span>                                                                          | <span data-ttu-id="0a6c2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a6c2-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="0a6c2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a6c2-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0a6c2-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0a6c2-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0a6c2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a6c2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6c2-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="0a6c2-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="0a6c2-123">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="0a6c2-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




