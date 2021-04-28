---
description: 'Método IMpeg2PsiParser:: GetPmtVersionNumber – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Método IMpeg2PsiParser:: GetPmtVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084554"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="601b6-104">Método IMpeg2PsiParser:: GetPmtVersionNumber</span><span class="sxs-lookup"><span data-stu-id="601b6-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="601b6-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="601b6-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="601b6-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="601b6-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="601b6-107">O `GetPmtVersionNumber` método recupera o \_ campo de número de versão de um PGTO especificado.</span><span class="sxs-lookup"><span data-stu-id="601b6-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="601b6-108">O número de versão é incrementado sempre que a definição do programa é alterada.</span><span class="sxs-lookup"><span data-stu-id="601b6-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="601b6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="601b6-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="601b6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="601b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601b6-111">*wProgramNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="601b6-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601b6-112">Especifica o \_ campo de número do programa do programa, conforme fornecido no Pat.</span><span class="sxs-lookup"><span data-stu-id="601b6-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="601b6-113">*pPmtVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="601b6-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="601b6-114">Ponteiro para uma variável que recebe o campo de número de versão \_ .</span><span class="sxs-lookup"><span data-stu-id="601b6-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601b6-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="601b6-115">Return value</span></span>

<span data-ttu-id="601b6-116">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="601b6-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="601b6-117">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="601b6-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="601b6-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="601b6-118">Return code</span></span>                                                                          | <span data-ttu-id="601b6-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="601b6-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="601b6-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="601b6-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="601b6-121">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="601b6-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="601b6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="601b6-122">Remarks</span></span>

<span data-ttu-id="601b6-123">Use o método **GetRecordProgramNumber** para obter o número do programa.</span><span class="sxs-lookup"><span data-stu-id="601b6-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="601b6-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="601b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601b6-125">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="601b6-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="601b6-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="601b6-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="601b6-127">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="601b6-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




