---
description: 'Saiba mais sobre: colunas marcadas, fixas e variáveis'
title: Colunas marcadas, fixas e variáveis
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461097"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="1482b-103">Colunas marcadas, fixas e variáveis</span><span class="sxs-lookup"><span data-stu-id="1482b-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="1482b-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1482b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="1482b-105">Colunas marcadas, fixas e variáveis</span><span class="sxs-lookup"><span data-stu-id="1482b-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="1482b-106">Colunas marcadas, fixas e de comprimento variável são os tipos de coluna principais com suporte do ESE.</span><span class="sxs-lookup"><span data-stu-id="1482b-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="1482b-107">As colunas marcadas não estão presentes em um registro, a menos que os dados sejam armazenados na coluna e possam ser fixos ou ter comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="1482b-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="1482b-108">As colunas marcadas também podem conter mais de um valor em um único registro.</span><span class="sxs-lookup"><span data-stu-id="1482b-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="1482b-109">As colunas fixas assumem a mesma quantidade de espaço em cada linha e exigem 1 bit para representar o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="1482b-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="1482b-110">Colunas de comprimento variável exigem 2 bytes para representar o tamanho e o valor nulo e ocupam uma quantidade variável de espaço em cada registro.</span><span class="sxs-lookup"><span data-stu-id="1482b-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="1482b-111">Para obter mais informações sobre as colunas marcadas e fixas, consulte a Jet_bitColumnTagged e Jet_bitColumnFixed opção no membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) usada na chamada para [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="1482b-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="1482b-112">Colunas de comprimento variável são determinadas pelo tipo de coluna que é definido no parâmetro *coltyp* na chamada de [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="1482b-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="1482b-113">Os tipos de coluna a seguir podem ser fixos ou ter comprimento variável, dependendo se a opção de Jet_bitColumnFixed está definida:</span><span class="sxs-lookup"><span data-stu-id="1482b-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="1482b-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="1482b-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="1482b-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="1482b-115">JET_coltypText</span></span>

  - <span data-ttu-id="1482b-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="1482b-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="1482b-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="1482b-117">JET_coltypLongText</span></span>

<span data-ttu-id="1482b-118">Em geral, os dados no registro são armazenados com o intervalo fixo primeiro, o intervalo de variáveis Next e o intervalo marcado armazenado por último.</span><span class="sxs-lookup"><span data-stu-id="1482b-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="1482b-119">O diagrama a seguir mostra como os registros são armazenados na tabela.</span><span class="sxs-lookup"><span data-stu-id="1482b-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="1482b-120">Conforme mostrado no diagrama, o intervalo marcado pode conter colunas com vários valores.</span><span class="sxs-lookup"><span data-stu-id="1482b-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="1482b-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="1482b-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
