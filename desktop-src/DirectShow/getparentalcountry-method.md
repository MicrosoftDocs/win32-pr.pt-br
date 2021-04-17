---
description: O método DVDAdm. GetParentalCountry recupera o país/região pai que foi salvo pela última vez no registro.
ms.assetid: 947c5e2a-dfd5-4900-87d4-0ec967b99a22
title: Método GetParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fcee63fd3cad64498d95ca74e81a9f02804a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748180"
---
# <a name="getparentalcountry-method"></a><span data-ttu-id="04bae-103">Método GetParentalCountry</span><span class="sxs-lookup"><span data-stu-id="04bae-103">GetParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="04bae-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="04bae-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="04bae-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="04bae-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="04bae-106">O `DVDAdm.GetParentalCountry` método recupera o país/região pai que foi salvo pela última vez no registro.</span><span class="sxs-lookup"><span data-stu-id="04bae-106">The `DVDAdm.GetParentalCountry` method retrieves the parental country/region that was last saved to the registry.</span></span>

``` syntax
[ iParentalCountry = ] DVD.DVDAdm.GetParentalCountry()
```

## <a name="return-value"></a><span data-ttu-id="04bae-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="04bae-107">Return Value</span></span>

<span data-ttu-id="04bae-108">Retorna um inteiro que indica o código de país/região padrão armazenado no registro.</span><span class="sxs-lookup"><span data-stu-id="04bae-108">Returns an Integer indicating the default country/region code stored in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bae-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="04bae-109">Remarks</span></span>

<span data-ttu-id="04bae-110">O país/região pai que esse método recupera não é necessariamente o mesmo país/região atualmente armazenado no objeto MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="04bae-110">The parental country/region this method retrieves is not necessarily the same country/region currently stored in the MSWebDVD object.</span></span>

## <a name="requirements"></a><span data-ttu-id="04bae-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04bae-111">Requirements</span></span>



| <span data-ttu-id="04bae-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bae-112">Requirement</span></span> | <span data-ttu-id="04bae-113">Valor</span><span class="sxs-lookup"><span data-stu-id="04bae-113">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04bae-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04bae-114">Header</span></span><br/> | <dl> <span data-ttu-id="04bae-115"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="04bae-115"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04bae-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="04bae-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bae-117">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="04bae-117">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




