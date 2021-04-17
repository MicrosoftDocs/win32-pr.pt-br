---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 35 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo de ação personalizada 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783274"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="79ab7-103">Tipo de ação personalizada 35</span><span class="sxs-lookup"><span data-stu-id="79ab7-103">Custom Action Type 35</span></span>

<span data-ttu-id="79ab7-104">Essa ação personalizada define o diretório de instalação de uma cadeia de caracteres de texto formatada.</span><span class="sxs-lookup"><span data-stu-id="79ab7-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="79ab7-105">Para obter mais informações, consulte [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)</span><span class="sxs-lookup"><span data-stu-id="79ab7-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="79ab7-106">Fonte</span><span class="sxs-lookup"><span data-stu-id="79ab7-106">Source</span></span>

<span data-ttu-id="79ab7-107">O campo de origem da [tabela CustomAction](customaction-table.md) contém uma chave para a [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="79ab7-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="79ab7-108">O diretório designado é definido pela cadeia de caracteres formatada no campo de destino usando [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span><span class="sxs-lookup"><span data-stu-id="79ab7-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="79ab7-109">Isso define o caminho de destino e a propriedade associada para o valor expandido da cadeia de caracteres de texto formatado no campo de destino.</span><span class="sxs-lookup"><span data-stu-id="79ab7-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="79ab7-110">Não tente alterar o local de um diretório de destino durante uma [instalação de manutenção](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="79ab7-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="79ab7-111">Não tente alterar o caminho do diretório de destino se alguns componentes que usam esse caminho já estiverem instalados para qualquer usuário.</span><span class="sxs-lookup"><span data-stu-id="79ab7-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="79ab7-112">Valor do tipo</span><span class="sxs-lookup"><span data-stu-id="79ab7-112">Type Value</span></span>

<span data-ttu-id="79ab7-113">Inclua o seguinte valor na coluna tipo da [tabela CustomAction](customaction-table.md) para especificar o tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="79ab7-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="79ab7-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="79ab7-114">Constants</span></span>                                                              | <span data-ttu-id="79ab7-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="79ab7-115">Hexadecimal</span></span> | <span data-ttu-id="79ab7-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="79ab7-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="79ab7-117">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="79ab7-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="79ab7-118">0x023</span><span class="sxs-lookup"><span data-stu-id="79ab7-118">0x023</span></span>       | <span data-ttu-id="79ab7-119">35</span><span class="sxs-lookup"><span data-stu-id="79ab7-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="79ab7-120">Destino</span><span class="sxs-lookup"><span data-stu-id="79ab7-120">Target</span></span>

<span data-ttu-id="79ab7-121">A coluna Target da [tabela CustomAction](customaction-table.md) contém uma cadeia de texto formatada usando a funcionalidade especificada em [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sem os especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="79ab7-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="79ab7-122">Os parâmetros a serem substituídos são colocados entre colchetes \[ ... \] e podem ser Propriedades, variáveis de ambiente (% Prefix), caminhos de arquivo ( \# prefixo) ou caminhos de diretório de componente ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="79ab7-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="79ab7-123">Observe que os caminhos de diretório sempre terminam com um separador de diretório.</span><span class="sxs-lookup"><span data-stu-id="79ab7-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="79ab7-124">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="79ab7-124">Return Processing Options</span></span>

<span data-ttu-id="79ab7-125">A ação personalizada não usa essas opções.</span><span class="sxs-lookup"><span data-stu-id="79ab7-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="79ab7-126">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="79ab7-126">Execution Scheduling Options</span></span>

<span data-ttu-id="79ab7-127">Inclua bits de sinalizador opcionais na coluna Type da [tabela CustomAction](customaction-table.md) para especificar opções de agendamento de execução.</span><span class="sxs-lookup"><span data-stu-id="79ab7-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="79ab7-128">Essas opções controlam a execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="79ab7-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="79ab7-129">Para obter uma descrição das opções, consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="79ab7-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="79ab7-130">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="79ab7-130">In-Script Execution Options</span></span>

<span data-ttu-id="79ab7-131">A ação personalizada não usa essas opções.</span><span class="sxs-lookup"><span data-stu-id="79ab7-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="79ab7-132">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="79ab7-132">Return Values</span></span>

<span data-ttu-id="79ab7-133">Consulte [valores de retorno de ação personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="79ab7-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79ab7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="79ab7-134">Remarks</span></span>

<span data-ttu-id="79ab7-135">Se você definir uma [propriedade privada](private-properties.md) na sequência da interface do usuário criando uma ação personalizada em uma das tabelas de sequência da interface do usuário, essa propriedade não será definida na sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="79ab7-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="79ab7-136">Para definir a propriedade na sequência de execução, você também deve colocar uma ação personalizada em uma tabela de sequência de execução.</span><span class="sxs-lookup"><span data-stu-id="79ab7-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="79ab7-137">Como alternativa, você pode tornar a propriedade uma [propriedade pública](public-properties.md) e incluí-la na [**Propriedade SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="79ab7-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79ab7-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79ab7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79ab7-139">\_Ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="79ab7-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="79ab7-140">Ações personalizadas de texto formatado</span><span class="sxs-lookup"><span data-stu-id="79ab7-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



