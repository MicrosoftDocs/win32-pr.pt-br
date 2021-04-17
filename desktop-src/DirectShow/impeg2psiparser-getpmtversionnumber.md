---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
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
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779522"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="26c56-104">Método IMpeg2PsiParser:: GetPmtVersionNumber</span><span class="sxs-lookup"><span data-stu-id="26c56-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="26c56-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="26c56-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="26c56-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="26c56-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="26c56-107">O `GetPmtVersionNumber` método recupera o \_ campo de número de versão de um PGTO especificado.</span><span class="sxs-lookup"><span data-stu-id="26c56-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="26c56-108">O número de versão é incrementado sempre que a definição do programa é alterada.</span><span class="sxs-lookup"><span data-stu-id="26c56-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c56-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26c56-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="26c56-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26c56-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c56-111">*wProgramNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="26c56-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c56-112">Especifica o \_ campo de número do programa do programa, conforme fornecido no Pat.</span><span class="sxs-lookup"><span data-stu-id="26c56-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="26c56-113">*pPmtVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="26c56-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26c56-114">Ponteiro para uma variável que recebe o campo de número de versão \_ .</span><span class="sxs-lookup"><span data-stu-id="26c56-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c56-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26c56-115">Return value</span></span>

<span data-ttu-id="26c56-116">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26c56-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="26c56-117">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="26c56-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="26c56-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="26c56-118">Return code</span></span>                                                                          | <span data-ttu-id="26c56-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="26c56-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="26c56-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26c56-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="26c56-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="26c56-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26c56-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="26c56-122">Remarks</span></span>

<span data-ttu-id="26c56-123">Use o método **GetRecordProgramNumber** para obter o número do programa.</span><span class="sxs-lookup"><span data-stu-id="26c56-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="26c56-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="26c56-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c56-125">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="26c56-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="26c56-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="26c56-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="26c56-127">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="26c56-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




