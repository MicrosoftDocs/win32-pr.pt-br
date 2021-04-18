---
description: Operadores de atribuição de multiplicação.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operador * = operadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810710"
---
# <a name="operator--operators"></a><span data-ttu-id="55b37-103">operador \* = operadores</span><span class="sxs-lookup"><span data-stu-id="55b37-103">operator \*= operators</span></span>

<span data-ttu-id="55b37-104">Operadores de atribuição de multiplicação</span><span class="sxs-lookup"><span data-stu-id="55b37-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="55b37-105">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="55b37-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="55b37-106">Operador</span><span class="sxs-lookup"><span data-stu-id="55b37-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="55b37-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55b37-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="55b37-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR:: Operator \* = (XMVECTOR&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="55b37-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="55b37-109">Multiplica uma <code>XMVECTOR</code> instância por um valor de ponto flutuante e retorna uma referência à instância atualizada.</span><span class="sxs-lookup"><span data-stu-id="55b37-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="55b37-110">O <code>operator \*=</code> multiplica cada componente da instância atual do tipo de <a href="xmvector-data-type.md"><strong>dados XMVECTOR</strong></a> por um valor de ponto flutuante especificado, retornando uma referência à instância atual atualizada.</span><span class="sxs-lookup"><span data-stu-id="55b37-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="55b37-111">Esse operador só está disponível em C++.</span><span class="sxs-lookup"><span data-stu-id="55b37-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="55b37-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR:: Operator \* = (XMVECTOR&, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="55b37-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="55b37-113">Multiplica uma <code>XMVECTOR</code> instância por uma segunda instância, retornando uma referência à instância inicial atualizada.</span><span class="sxs-lookup"><span data-stu-id="55b37-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="55b37-114">O <code>operator \*=</code> multiplica cada componente da instância atual do tipo de <a href="xmvector-data-type.md"><strong>dados XMVECTOR</strong></a> pelo componente correspondente em uma segunda instância especificada do <code>XMVECTOR</code> , retornando uma referência à instância inicial atualizada.</span><span class="sxs-lookup"><span data-stu-id="55b37-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="55b37-115">Esse operador só está disponível em C++.</span><span class="sxs-lookup"><span data-stu-id="55b37-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="55b37-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="55b37-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b37-117">Operadores XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="55b37-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="55b37-118">**Referência**</span><span class="sxs-lookup"><span data-stu-id="55b37-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55b37-119">**Tipo de dados XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="55b37-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
