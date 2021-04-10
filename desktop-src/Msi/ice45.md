---
description: ICE45 valida que as colunas de campo de bits no banco de dados não definem nenhum bit reservado como 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169191"
---
# <a name="ice45"></a><span data-ttu-id="4c727-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="4c727-103">ICE45</span></span>

<span data-ttu-id="4c727-104">ICE45 valida que as colunas de campo de bits no banco de dados não definem nenhum bit reservado como 1.</span><span class="sxs-lookup"><span data-stu-id="4c727-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="4c727-105">Os bits reservados não fornecem nenhuma funcionalidade nas versões atuais do instalador, mas podem estar em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="4c727-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="4c727-106">Eles devem ser definidos como 0 para serem compatíveis com as versões futuras do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4c727-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="4c727-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="4c727-107">Result</span></span>

<span data-ttu-id="4c727-108">ICE45 posta uma mensagem de erro se qualquer uma das tabelas a seguir contiver um campo de bits com um bit reservado definido como um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="4c727-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="4c727-109">Tabela BBControl</span><span class="sxs-lookup"><span data-stu-id="4c727-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="4c727-110">Tabela de diálogo</span><span class="sxs-lookup"><span data-stu-id="4c727-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="4c727-111">Tabela de recursos</span><span class="sxs-lookup"><span data-stu-id="4c727-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="4c727-112">Tabela de arquivos</span><span class="sxs-lookup"><span data-stu-id="4c727-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="4c727-113">Tabela MoveFile</span><span class="sxs-lookup"><span data-stu-id="4c727-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="4c727-114">Tabela ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c727-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="4c727-115">Tabela ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="4c727-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="4c727-116">Tabela de patches</span><span class="sxs-lookup"><span data-stu-id="4c727-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="4c727-117">Remover tabelafile</span><span class="sxs-lookup"><span data-stu-id="4c727-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="4c727-118">Tabela de UserControl</span><span class="sxs-lookup"><span data-stu-id="4c727-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="4c727-119">Tabela de desinstalação</span><span class="sxs-lookup"><span data-stu-id="4c727-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="4c727-120">Tabela TextStyle</span><span class="sxs-lookup"><span data-stu-id="4c727-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="4c727-121">ICE45 posta uma das duas mensagens de aviso se a [tabela de controle](control-table.md) contiver um campo de bits com um bit reservado definido como um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="4c727-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="4c727-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c727-122">Example</span></span>

<span data-ttu-id="4c727-123">ICE45 relata o seguinte erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="4c727-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="4c727-124">ICE45 relata o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="4c727-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="4c727-125">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4c727-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="4c727-126">Arquivo</span><span class="sxs-lookup"><span data-stu-id="4c727-126">File</span></span>  | <span data-ttu-id="4c727-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c727-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="4c727-128">Arquivo1</span><span class="sxs-lookup"><span data-stu-id="4c727-128">File1</span></span> | <span data-ttu-id="4c727-129">128</span><span class="sxs-lookup"><span data-stu-id="4c727-129">128</span></span>        |



 

<span data-ttu-id="4c727-130">[Tabela de controle](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4c727-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="4c727-131">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="4c727-131">Dialog</span></span>  | <span data-ttu-id="4c727-132">Control</span><span class="sxs-lookup"><span data-stu-id="4c727-132">Control</span></span> | <span data-ttu-id="4c727-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c727-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="4c727-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="4c727-134">Dialog1</span></span> | <span data-ttu-id="4c727-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="4c727-135">Edit1</span></span>   | <span data-ttu-id="4c727-136">2097152</span><span class="sxs-lookup"><span data-stu-id="4c727-136">2097152</span></span>    |
| <span data-ttu-id="4c727-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="4c727-137">Dialog1</span></span> | <span data-ttu-id="4c727-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="4c727-138">Edit2</span></span>   | <span data-ttu-id="4c727-139">1048576</span><span class="sxs-lookup"><span data-stu-id="4c727-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="4c727-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c727-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c727-141">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="4c727-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



