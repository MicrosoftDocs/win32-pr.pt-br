---
description: Operadores de multiplicação.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operadores do operador *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091087"
---
# <a name="operator--operators"></a><span data-ttu-id="e5408-103">operadores de operador \*</span><span class="sxs-lookup"><span data-stu-id="e5408-103">operator \* operators</span></span>

<span data-ttu-id="e5408-104">Operadores de multiplicação</span><span class="sxs-lookup"><span data-stu-id="e5408-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="e5408-105">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="e5408-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e5408-106">Operador</span><span class="sxs-lookup"><span data-stu-id="e5408-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e5408-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5408-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5408-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR:: Operator \* (float, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5408-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5408-109">Multiplique um valor de ponto flutuante por uma instância do <code>XMVECTOR</code> , retornando o resultado de uma nova instância do <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="e5408-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="e5408-110">O <code>operator \*</code> multiplica um valor de ponto flutuante em relação a cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a>, retornando uma nova <code>XMVECTOR</code> instância cujos componentes contêm o resultado.</span><span class="sxs-lookup"><span data-stu-id="e5408-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e5408-111">Esse operador só está disponível em C++.</span><span class="sxs-lookup"><span data-stu-id="e5408-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e5408-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR:: Operator \* (XMVECTOR, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5408-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5408-113">Multiplique uma instância de <code>XMVECTOR</code> por um valor de ponto flutuante, retornando o resultado de uma nova instância do <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="e5408-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="e5408-114">O <code>operator \*</code> multiplica cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a> por um valor de ponto flutuante, retornando uma nova <code>XMVECTOR</code> instância cujos componentes contêm o resultado.</span><span class="sxs-lookup"><span data-stu-id="e5408-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e5408-115">Esse operador só está disponível em C++.</span><span class="sxs-lookup"><span data-stu-id="e5408-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e5408-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR:: Operator \* (XMVECTOR, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e5408-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e5408-117">Multiplica uma instância de <code>XMVECTOR</code> por uma segunda instância, retornando o resultado em uma terceira instância.</span><span class="sxs-lookup"><span data-stu-id="e5408-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="e5408-118">O <code>operator \*</code> multiplica cada componente de uma instância do <a href="xmvector-data-type.md"><strong>tipo de dados XMVECTOR</strong></a> pelo componente correspondente em uma segunda instância do <code>XMVECTOR</code> , retornando uma nova <code>XMVECTOR</code> instância que contém o resultado.</span><span class="sxs-lookup"><span data-stu-id="e5408-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e5408-119">Esse operador só está disponível em C++.</span><span class="sxs-lookup"><span data-stu-id="e5408-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="e5408-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5408-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5408-121">Operadores XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="e5408-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="e5408-122">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e5408-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5408-123">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="e5408-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
