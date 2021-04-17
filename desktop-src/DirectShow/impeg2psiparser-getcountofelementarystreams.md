---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Método IMpeg2PsiParser:: GetCountOfElementaryStreams'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754761"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="c2e03-104">Método IMpeg2PsiParser:: GetCountOfElementaryStreams</span><span class="sxs-lookup"><span data-stu-id="c2e03-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="c2e03-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c2e03-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c2e03-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="c2e03-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c2e03-107">O `GetCountOfElementaryStreams` método recupera o número de fluxos elementares em um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="c2e03-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e03-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2e03-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="c2e03-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2e03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e03-110">*wProgramNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2e03-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e03-111">Especifica o \_ campo de número do programa para o programa, conforme fornecido no Pat.</span><span class="sxs-lookup"><span data-stu-id="c2e03-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="c2e03-112">*pwVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2e03-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e03-113">Ponteiro para uma variável que recebe o número de fluxos elementares no programa.</span><span class="sxs-lookup"><span data-stu-id="c2e03-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e03-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2e03-114">Return value</span></span>

<span data-ttu-id="c2e03-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2e03-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c2e03-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c2e03-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c2e03-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c2e03-117">Return code</span></span>                                                                          | <span data-ttu-id="c2e03-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c2e03-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c2e03-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2e03-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2e03-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c2e03-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2e03-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2e03-121">Remarks</span></span>

<span data-ttu-id="c2e03-122">Use o método **GetRecordProgramNumber** para obter o número do programa.</span><span class="sxs-lookup"><span data-stu-id="c2e03-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2e03-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2e03-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e03-124">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="c2e03-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c2e03-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="c2e03-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="c2e03-126">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="c2e03-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




