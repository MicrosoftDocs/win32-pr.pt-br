---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Método IMpeg2PsiParser:: GetTransportStreamId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754243"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="c66d1-104">Método IMpeg2PsiParser:: GetTransportStreamId</span><span class="sxs-lookup"><span data-stu-id="c66d1-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="c66d1-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c66d1-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c66d1-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="c66d1-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c66d1-107">O `GetTransportStreamId` método recupera o \_ \_ campo ID do fluxo de transporte do Pat.</span><span class="sxs-lookup"><span data-stu-id="c66d1-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="c66d1-108">Esse valor é definido pelo usuário e pode ser usado para distinguir um fluxo de transporte específico de outros fluxos na mesma rede.</span><span class="sxs-lookup"><span data-stu-id="c66d1-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="c66d1-109">Um fluxo de transporte contém no máximo uma PAT.</span><span class="sxs-lookup"><span data-stu-id="c66d1-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c66d1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c66d1-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="c66d1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c66d1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c66d1-112">*pStreamId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c66d1-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c66d1-113">Ponteiro para uma variável que recebe o \_ campo ID do fluxo de transporte \_ .</span><span class="sxs-lookup"><span data-stu-id="c66d1-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c66d1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c66d1-114">Return value</span></span>

<span data-ttu-id="c66d1-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c66d1-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c66d1-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c66d1-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c66d1-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c66d1-117">Return code</span></span>                                                                          | <span data-ttu-id="c66d1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c66d1-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c66d1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c66d1-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c66d1-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c66d1-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c66d1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c66d1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66d1-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="c66d1-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c66d1-123">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="c66d1-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




