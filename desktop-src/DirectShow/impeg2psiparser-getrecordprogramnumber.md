---
description: 'Método IMpeg2PsiParser:: GetRecordProgramNumber – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
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
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089134"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="61df6-104">Método IMpeg2PsiParser:: GetRecordProgramNumber</span><span class="sxs-lookup"><span data-stu-id="61df6-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="61df6-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="61df6-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="61df6-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="61df6-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="61df6-107">O `GetRecordProgramNumber` método recupera o número do programa para um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="61df6-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="61df6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61df6-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="61df6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61df6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61df6-110">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61df6-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61df6-111">Especifica a entrada no PAT que define o programa, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="61df6-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="61df6-112">*pwVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61df6-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61df6-113">Ponteiro para uma variável que recebe o \_ campo de número do programa do Pat.</span><span class="sxs-lookup"><span data-stu-id="61df6-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61df6-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="61df6-114">Return value</span></span>

<span data-ttu-id="61df6-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61df6-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="61df6-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="61df6-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="61df6-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="61df6-117">Return code</span></span>                                                                          | <span data-ttu-id="61df6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="61df6-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="61df6-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61df6-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="61df6-120">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="61df6-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="61df6-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="61df6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61df6-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="61df6-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="61df6-123">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="61df6-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




