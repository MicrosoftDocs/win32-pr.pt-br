---
description: 'Método IMpeg2PsiParser:: GetCountOfPrograms – a implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow. Não é uma API do DirectShow com suporte.'
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
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119424"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="f2e3f-104">Método IMpeg2PsiParser:: GetCountOfPrograms</span><span class="sxs-lookup"><span data-stu-id="f2e3f-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="f2e3f-105">A implementação desse método é fornecida como um código de exemplo com o SDK do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="f2e3f-106">Não é uma API do DirectShow com suporte.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="f2e3f-107">O `GetCountOfPrograms` método recupera o número de programas no fluxo de transporte.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e3f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e3f-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="f2e3f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e3f-110">*pNumOfPrograms* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f2e3f-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e3f-111">Ponteiro para uma variável que recebe o número de programas.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e3f-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f2e3f-112">Return value</span></span>

<span data-ttu-id="f2e3f-113">O método retorna um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="f2e3f-114">Os valores possíveis incluem, mas não se limitam a, os valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="f2e3f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f2e3f-115">Return code</span></span>                                                                          | <span data-ttu-id="f2e3f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2e3f-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f2e3f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2e3f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f2e3f-118">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="f2e3f-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f2e3f-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f2e3f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e3f-120">**Interface IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="f2e3f-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="f2e3f-121">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="f2e3f-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




