---
description: A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Método IMpeg2PsiParser:: GetPatVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370115"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="21740-104">Método IMpeg2PsiParser:: GetPatVersionNumber</span><span class="sxs-lookup"><span data-stu-id="21740-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="21740-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="21740-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="21740-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="21740-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="21740-107">O `GetPatVersionNumber` método recupera o \_ campo de número de versão do Pat.</span><span class="sxs-lookup"><span data-stu-id="21740-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="21740-108">Um fluxo de transporte contém no máximo uma PAT.</span><span class="sxs-lookup"><span data-stu-id="21740-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="21740-109">O número de versão é incrementado sempre que as informações na tabela são alteradas.</span><span class="sxs-lookup"><span data-stu-id="21740-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="21740-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21740-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="21740-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21740-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21740-112">*pPatVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21740-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21740-113">Ponteiro para uma variável que recebe o campo de número de versão \_ .</span><span class="sxs-lookup"><span data-stu-id="21740-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21740-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21740-114">Return value</span></span>

<span data-ttu-id="21740-115">O método retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21740-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="21740-116">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="21740-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="21740-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="21740-117">Return code</span></span>                                                                          | <span data-ttu-id="21740-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="21740-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="21740-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21740-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="21740-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="21740-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="21740-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="21740-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21740-122">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="21740-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="21740-123">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="21740-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




