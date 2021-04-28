---
description: 'Método IMpeg2PsiParser:: GetCountOfElementaryStreams – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
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
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089154"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="2d53a-104">Método IMpeg2PsiParser:: GetCountOfElementaryStreams</span><span class="sxs-lookup"><span data-stu-id="2d53a-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="2d53a-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2d53a-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="2d53a-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="2d53a-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="2d53a-107">O `GetCountOfElementaryStreams` método recupera o número de fluxos elementares em um programa especificado.</span><span class="sxs-lookup"><span data-stu-id="2d53a-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d53a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d53a-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="2d53a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d53a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d53a-110">*wProgramNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d53a-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d53a-111">Especifica o \_ campo de número do programa para o programa, conforme fornecido no Pat.</span><span class="sxs-lookup"><span data-stu-id="2d53a-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="2d53a-112">*pwVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2d53a-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d53a-113">Ponteiro para uma variável que recebe o número de fluxos elementares no programa.</span><span class="sxs-lookup"><span data-stu-id="2d53a-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d53a-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2d53a-114">Return value</span></span>

<span data-ttu-id="2d53a-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2d53a-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="2d53a-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d53a-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="2d53a-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2d53a-117">Return code</span></span>                                                                          | <span data-ttu-id="2d53a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d53a-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="2d53a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d53a-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2d53a-120">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="2d53a-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d53a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d53a-121">Remarks</span></span>

<span data-ttu-id="2d53a-122">Use o método **GetRecordProgramNumber** para obter o número do programa.</span><span class="sxs-lookup"><span data-stu-id="2d53a-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d53a-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d53a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d53a-124">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="2d53a-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="2d53a-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="2d53a-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="2d53a-126">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="2d53a-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




