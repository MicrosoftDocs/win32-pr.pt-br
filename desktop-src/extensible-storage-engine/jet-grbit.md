---
description: 'Saiba mais sobre: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "105753507"
---
# <a name="jet_grbit"></a><span data-ttu-id="b6e7e-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b6e7e-103">JET_GRBIT</span></span>


<span data-ttu-id="b6e7e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b6e7e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="b6e7e-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b6e7e-105">JET_GRBIT</span></span>

<span data-ttu-id="b6e7e-106">O tipo de dados **JET_GRBIT** é um grupo de bits que contém constantes específicas para as funções e estruturas nas quais ele é usado.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="b6e7e-107">Tipos de dados</span><span class="sxs-lookup"><span data-stu-id="b6e7e-107">Data Types</span></span>

<span data-ttu-id="b6e7e-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b6e7e-108">JET_GRBIT</span></span>

<span data-ttu-id="b6e7e-109">Em geral, as constantes usadas como valores para esse tipo de dados refletem o nome do elemento de API no qual elas são usadas.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="b6e7e-110">Por exemplo, todas as constantes passadas para [JetRetrieveColumn](./jetretrievecolumn-function.md) começam com "JET_bitRetrieve".</span><span class="sxs-lookup"><span data-stu-id="b6e7e-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="b6e7e-111">Da mesma forma, todas as constantes passadas para [JetSetColumn](./jetsetcolumn-function.md) começam com "JET_bitSet".</span><span class="sxs-lookup"><span data-stu-id="b6e7e-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="b6e7e-112">Um valor de zero faz com que o parâmetro seja ignorado.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="b6e7e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6e7e-113">Remarks</span></span>

<span data-ttu-id="b6e7e-114">Para obter mais informações, consulte a função ou estrutura específica.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="b6e7e-115">As opções geralmente são passadas como um conjunto de sinalizadores que podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="b6e7e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e7e-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6e7e-117"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b6e7e-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e7e-118">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6e7e-119"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="b6e7e-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e7e-120">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6e7e-121"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="b6e7e-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e7e-122">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b6e7e-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b6e7e-123">See Also</span></span>

[<span data-ttu-id="b6e7e-124">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b6e7e-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="b6e7e-125">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="b6e7e-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
