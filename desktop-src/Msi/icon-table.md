---
description: Esta tabela contém os arquivos de ícone. Cada ícone da tabela é copiado para um arquivo como parte do anúncio do produto a ser usado para atalhos anunciados e servidores OLE. Consulte limitações de OLE em fluxos.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabela de ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169189"
---
# <a name="icon-table"></a><span data-ttu-id="c0a74-105">Tabela de ícones</span><span class="sxs-lookup"><span data-stu-id="c0a74-105">Icon Table</span></span>

<span data-ttu-id="c0a74-106">Esta tabela contém os arquivos de ícone.</span><span class="sxs-lookup"><span data-stu-id="c0a74-106">This table contains the icon files.</span></span> <span data-ttu-id="c0a74-107">Cada ícone da tabela é copiado para um arquivo como parte do anúncio do produto a ser usado para atalhos anunciados e servidores OLE.</span><span class="sxs-lookup"><span data-stu-id="c0a74-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="c0a74-108">Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="c0a74-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="c0a74-109">A tabela de ícones tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0a74-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="c0a74-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="c0a74-110">Column</span></span> | <span data-ttu-id="c0a74-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0a74-111">Type</span></span>                         | <span data-ttu-id="c0a74-112">Chave</span><span class="sxs-lookup"><span data-stu-id="c0a74-112">Key</span></span> | <span data-ttu-id="c0a74-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="c0a74-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="c0a74-114">Nome</span><span class="sxs-lookup"><span data-stu-id="c0a74-114">Name</span></span>   | [<span data-ttu-id="c0a74-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="c0a74-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="c0a74-116">S</span><span class="sxs-lookup"><span data-stu-id="c0a74-116">Y</span></span>   | <span data-ttu-id="c0a74-117">N</span><span class="sxs-lookup"><span data-stu-id="c0a74-117">N</span></span>        |
| <span data-ttu-id="c0a74-118">Dados</span><span class="sxs-lookup"><span data-stu-id="c0a74-118">Data</span></span>   | [<span data-ttu-id="c0a74-119">Binary</span><span class="sxs-lookup"><span data-stu-id="c0a74-119">Binary</span></span>](binary.md)         | <span data-ttu-id="c0a74-120">N</span><span class="sxs-lookup"><span data-stu-id="c0a74-120">N</span></span>   | <span data-ttu-id="c0a74-121">N</span><span class="sxs-lookup"><span data-stu-id="c0a74-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c0a74-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="c0a74-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c0a74-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="c0a74-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="c0a74-124">Nome do arquivo de ícone.</span><span class="sxs-lookup"><span data-stu-id="c0a74-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="c0a74-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="c0a74-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="c0a74-126">Os dados do ícone binário no formato PE (. dll ou. exe) ou ícone (. ico).</span><span class="sxs-lookup"><span data-stu-id="c0a74-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0a74-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0a74-127">Remarks</span></span>

<span data-ttu-id="c0a74-128">Essa tabela é referida quando a [ação PublishProduct](publishproduct-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="c0a74-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="c0a74-129">Os ícones para atalhos, extensões de nome de arquivo e CLSIDs devem ser armazenados em arquivos separados do próprio arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="c0a74-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="c0a74-130">Isso é necessário porque o instalador deve copiar apenas os arquivos de ícone pequeno para o computador do usuário ao anunciar o recurso.</span><span class="sxs-lookup"><span data-stu-id="c0a74-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="c0a74-131">Portanto, um desenvolvedor de um pacote de instalação precisa criar arquivos separados contendo apenas os ícones.</span><span class="sxs-lookup"><span data-stu-id="c0a74-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="c0a74-132">Esses arquivos de ícone são armazenados como dados binários na tabela de ícones.</span><span class="sxs-lookup"><span data-stu-id="c0a74-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="c0a74-133">Os arquivos de ícone que estão associados estritamente com extensões de nome de arquivo ou CLSIDs podem ter qualquer extensão, como. ico.</span><span class="sxs-lookup"><span data-stu-id="c0a74-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="c0a74-134">No entanto, os arquivos de ícone associados a atalhos devem estar no formato binário EXE e devem ser nomeados de forma que sua extensão corresponda à extensão do destino.</span><span class="sxs-lookup"><span data-stu-id="c0a74-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="c0a74-135">O atalho não funcionará se essa regra não for seguida.</span><span class="sxs-lookup"><span data-stu-id="c0a74-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="c0a74-136">Por exemplo, se um atalho for apontar para um recurso com o arquivo de chave Red.bar, o arquivo de ícone também deverá ter a extensão. bar.</span><span class="sxs-lookup"><span data-stu-id="c0a74-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="c0a74-137">Vários ícones podem ser inserida no mesmo arquivo de ícone, desde que todos os arquivos de destino tenham a mesma extensão.</span><span class="sxs-lookup"><span data-stu-id="c0a74-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="c0a74-138">Validação</span><span class="sxs-lookup"><span data-stu-id="c0a74-138">Validation</span></span>

<dl>

[<span data-ttu-id="c0a74-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="c0a74-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c0a74-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="c0a74-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c0a74-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="c0a74-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="c0a74-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="c0a74-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c0a74-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="c0a74-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="c0a74-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="c0a74-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



