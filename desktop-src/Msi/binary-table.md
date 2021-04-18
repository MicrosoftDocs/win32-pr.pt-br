---
description: A tabela binária contém os dados binários de itens como bitmaps, animações e ícones. A tabela binária também é usada para armazenar dados para ações personalizadas. Consulte limitações de OLE em fluxos.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabela binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778732"
---
# <a name="binary-table"></a><span data-ttu-id="cdffb-105">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="cdffb-105">Binary Table</span></span>

<span data-ttu-id="cdffb-106">A tabela binária contém os dados binários de itens como bitmaps, animações e ícones.</span><span class="sxs-lookup"><span data-stu-id="cdffb-106">The Binary table holds the binary data for items such as bitmaps, animations, and icons.</span></span> <span data-ttu-id="cdffb-107">A tabela binária também é usada para armazenar dados para ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="cdffb-107">The binary table is also used to store data for custom actions.</span></span> <span data-ttu-id="cdffb-108">Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="cdffb-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="cdffb-109">A tabela binária tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="cdffb-109">The Binary table has the following columns.</span></span>



| <span data-ttu-id="cdffb-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="cdffb-110">Column</span></span> | <span data-ttu-id="cdffb-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cdffb-111">Type</span></span>                         | <span data-ttu-id="cdffb-112">Chave</span><span class="sxs-lookup"><span data-stu-id="cdffb-112">Key</span></span> | <span data-ttu-id="cdffb-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="cdffb-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="cdffb-114">Nome</span><span class="sxs-lookup"><span data-stu-id="cdffb-114">Name</span></span>   | [<span data-ttu-id="cdffb-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="cdffb-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="cdffb-116">S</span><span class="sxs-lookup"><span data-stu-id="cdffb-116">Y</span></span>   | <span data-ttu-id="cdffb-117">N</span><span class="sxs-lookup"><span data-stu-id="cdffb-117">N</span></span>        |
| <span data-ttu-id="cdffb-118">Dados</span><span class="sxs-lookup"><span data-stu-id="cdffb-118">Data</span></span>   | [<span data-ttu-id="cdffb-119">Binary</span><span class="sxs-lookup"><span data-stu-id="cdffb-119">Binary</span></span>](binary.md)         | <span data-ttu-id="cdffb-120">N</span><span class="sxs-lookup"><span data-stu-id="cdffb-120">N</span></span>   | <span data-ttu-id="cdffb-121">N</span><span class="sxs-lookup"><span data-stu-id="cdffb-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cdffb-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="cdffb-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cdffb-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="cdffb-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="cdffb-124">Uma chave exclusiva que identifica os dados binários específicos.</span><span class="sxs-lookup"><span data-stu-id="cdffb-124">A unique key that identifies the particular binary data.</span></span> <span data-ttu-id="cdffb-125">Se os dados binários forem para um controle, a chave aparecerá na coluna de texto do controle associado na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="cdffb-125">If the binary data is for a control, the key appears in the Text column of the associated control in the [Control table](control-table.md).</span></span> <span data-ttu-id="cdffb-126">Essa chave deve ser exclusiva entre todos os controles que exigem dados binários.</span><span class="sxs-lookup"><span data-stu-id="cdffb-126">This key must be unique among all controls requiring binary data.</span></span>

</dd> <dt>

<span data-ttu-id="cdffb-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="cdffb-127"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="cdffb-128">Os dados binários não formatados.</span><span class="sxs-lookup"><span data-stu-id="cdffb-128">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="cdffb-129">Validação</span><span class="sxs-lookup"><span data-stu-id="cdffb-129">Validation</span></span>

<dl>

[<span data-ttu-id="cdffb-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="cdffb-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cdffb-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="cdffb-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cdffb-132">ICE17</span><span class="sxs-lookup"><span data-stu-id="cdffb-132">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="cdffb-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="cdffb-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



