---
description: A tabela ReserveCost é uma tabela opcional que permite que o autor Reserve uma quantidade de espaço em disco em qualquer diretório que dependa do estado de instalação de um componente.
ms.assetid: 371e72f1-40a2-4ed2-b0ab-33840075ff47
title: Tabela ReserveCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f593fd11789cd2304385b97e96e50a009fbde0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921963"
---
# <a name="reservecost-table"></a><span data-ttu-id="9e47c-103">Tabela ReserveCost</span><span class="sxs-lookup"><span data-stu-id="9e47c-103">ReserveCost Table</span></span>

<span data-ttu-id="9e47c-104">A tabela ReserveCost é uma tabela opcional que permite que o autor Reserve uma quantidade de espaço em disco em qualquer diretório que dependa do estado de instalação de um componente.</span><span class="sxs-lookup"><span data-stu-id="9e47c-104">The ReserveCost table is an optional table that allows the author to reserve an amount of disk space in any directory that depends on the installation state of a component.</span></span>

<span data-ttu-id="9e47c-105">A tabela ReserveCost tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e47c-105">The ReserveCost table has the following columns.</span></span>



| <span data-ttu-id="9e47c-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="9e47c-106">Column</span></span>        | <span data-ttu-id="9e47c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e47c-107">Type</span></span>                               | <span data-ttu-id="9e47c-108">Chave</span><span class="sxs-lookup"><span data-stu-id="9e47c-108">Key</span></span> | <span data-ttu-id="9e47c-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="9e47c-109">Nullable</span></span> |
|---------------|------------------------------------|-----|----------|
| <span data-ttu-id="9e47c-110">ReserveKey</span><span class="sxs-lookup"><span data-stu-id="9e47c-110">ReserveKey</span></span>    | [<span data-ttu-id="9e47c-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="9e47c-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9e47c-112">S</span><span class="sxs-lookup"><span data-stu-id="9e47c-112">Y</span></span>   | <span data-ttu-id="9e47c-113">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-113">N</span></span>        |
| <span data-ttu-id="9e47c-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="9e47c-114">Component\_</span></span>   | [<span data-ttu-id="9e47c-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="9e47c-115">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9e47c-116">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-116">N</span></span>   | <span data-ttu-id="9e47c-117">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-117">N</span></span>        |
| <span data-ttu-id="9e47c-118">ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="9e47c-118">ReserveFolder</span></span> | [<span data-ttu-id="9e47c-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="9e47c-119">Identifier</span></span>](identifier.md)       | <span data-ttu-id="9e47c-120">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-120">N</span></span>   | <span data-ttu-id="9e47c-121">S</span><span class="sxs-lookup"><span data-stu-id="9e47c-121">Y</span></span>        |
| <span data-ttu-id="9e47c-122">ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="9e47c-122">ReserveLocal</span></span>  | [<span data-ttu-id="9e47c-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9e47c-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9e47c-124">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-124">N</span></span>   | <span data-ttu-id="9e47c-125">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-125">N</span></span>        |
| <span data-ttu-id="9e47c-126">Conservar</span><span class="sxs-lookup"><span data-stu-id="9e47c-126">ReserveSource</span></span> | [<span data-ttu-id="9e47c-127">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="9e47c-127">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="9e47c-128">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-128">N</span></span>   | <span data-ttu-id="9e47c-129">N</span><span class="sxs-lookup"><span data-stu-id="9e47c-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9e47c-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="9e47c-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9e47c-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span><span class="sxs-lookup"><span data-stu-id="9e47c-131"><span id="ReserveKey"></span><span id="reservekey"></span><span id="RESERVEKEY"></span>ReserveKey</span></span>
</dt> <dd>

<span data-ttu-id="9e47c-132">Chave primária que identifica exclusivamente uma entrada de tabela ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="9e47c-132">Primary key that uniquely identifies a ReserveCost table entry.</span></span>

</dd> <dt>

<span data-ttu-id="9e47c-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="9e47c-133"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9e47c-134">Chave externa para a coluna um da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9e47c-134">External key to column one of the [Component](component-table.md) table.</span></span> <span data-ttu-id="9e47c-135">Reserva uma quantidade especificada de espaço se este componente deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="9e47c-135">Reserves a specified amount of space if this component is to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="9e47c-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span><span class="sxs-lookup"><span data-stu-id="9e47c-136"><span id="ReserveFolder"></span><span id="reservefolder"></span><span id="RESERVEFOLDER"></span>ReserveFolder</span></span>
</dt> <dd>

<span data-ttu-id="9e47c-137">Esta coluna contém o nome de uma propriedade que é o caminho completo para o diretório de destino.</span><span class="sxs-lookup"><span data-stu-id="9e47c-137">This column contains the name of a property that is the full path to the destination directory.</span></span> <span data-ttu-id="9e47c-138">Esse nome de propriedade normalmente é o nome de um diretório na tabela de [diretório](directory-table.md) ou o nome de um conjunto de propriedades obtido usando a ação [Appsearch](appsearch-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9e47c-138">This property name is typically the name of a directory in the [Directory](directory-table.md) table or the name of a property set obtained using the [Appsearch](appsearch-action.md) action.</span></span> <span data-ttu-id="9e47c-139">Isso adiciona a quantidade de espaço em disco especificada em ReserveLocal ou o inserve para o custo de volume do dispositivo que contém o diretório.</span><span class="sxs-lookup"><span data-stu-id="9e47c-139">This adds the amount of disk space specified in ReserveLocal or ReserveSource to the volume cost of the device containing the directory.</span></span>

</dd> <dt>

<span data-ttu-id="9e47c-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span><span class="sxs-lookup"><span data-stu-id="9e47c-140"><span id="ReserveLocal"></span><span id="reservelocal"></span><span id="RESERVELOCAL"></span>ReserveLocal</span></span>
</dt> <dd>

<span data-ttu-id="9e47c-141">O número de bytes de espaço em disco a ser reservado se o componente vinculado estiver instalado para ser executado localmente.</span><span class="sxs-lookup"><span data-stu-id="9e47c-141">The number of bytes of disk space to reserve if the linked component is installed to run locally.</span></span>

</dd> <dt>

<span data-ttu-id="9e47c-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>Conservar</span><span class="sxs-lookup"><span data-stu-id="9e47c-142"><span id="ReserveSource"></span><span id="reservesource"></span><span id="RESERVESOURCE"></span>ReserveSource</span></span>
</dt> <dd>

<span data-ttu-id="9e47c-143">O número de bytes de espaço em disco a ser reservado se o componente vinculado estiver instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="9e47c-143">The number of bytes of disk space to reserve if the linked component is installed to run from source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e47c-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e47c-144">Remarks</span></span>

<span data-ttu-id="9e47c-145">Reservar custos dessa maneira pode ser útil para autores que desejam garantir que uma quantidade mínima de espaço em disco estará disponível depois que a instalação for concluída.</span><span class="sxs-lookup"><span data-stu-id="9e47c-145">Reserving cost in this way could be useful for authors who want to ensure that a minimum amount of disk space will be available after the installation is completed.</span></span> <span data-ttu-id="9e47c-146">Por exemplo, esse espaço em disco pode ser reservado para documentos de usuário ou para arquivos de aplicativo (como arquivos de índice) que são criados somente depois que o aplicativo é iniciado após a instalação.</span><span class="sxs-lookup"><span data-stu-id="9e47c-146">For example, this disk space might be reserved for user documents or for application files (such as index files) that are created only after the application is started following installation.</span></span>

<span data-ttu-id="9e47c-147">Você pode usar a tabela ReserveCost para habilitar ações personalizadas para especificar um custo aproximado para quaisquer arquivos, entradas de registro ou outros itens que a ação personalizada possa instalar.</span><span class="sxs-lookup"><span data-stu-id="9e47c-147">You can use the ReserveCost table to enable custom actions to specify an approximate cost for any files, registry entries, or other items that the custom action might install.</span></span> <span data-ttu-id="9e47c-148">As ações personalizadas que adicionam entradas à tabela ReserveCost devem ser sequenciadas entre as ações [CostInitialize](costinitialize-action.md) e [filecost](filecost-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9e47c-148">Custom actions that add entries to the ReserveCost table should be sequenced between the [CostInitialize](costinitialize-action.md) and [FileCost](filecost-action.md) actions.</span></span> <span data-ttu-id="9e47c-149">Isso é necessário para a ação filecost inicializar corretamente o custo de todos os componentes afetados pelas entradas na tabela ReserveCost.</span><span class="sxs-lookup"><span data-stu-id="9e47c-149">This is necessary for the FileCost action to correctly initialize the costing of all components affected by entries in the ReserveCost table.</span></span>

## <a name="validation"></a><span data-ttu-id="9e47c-150">Validação</span><span class="sxs-lookup"><span data-stu-id="9e47c-150">Validation</span></span>

<dl>

[<span data-ttu-id="9e47c-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="9e47c-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9e47c-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="9e47c-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9e47c-153">ICE32</span><span class="sxs-lookup"><span data-stu-id="9e47c-153">ICE32</span></span>](ice32.md)  
</dl>

 

 



