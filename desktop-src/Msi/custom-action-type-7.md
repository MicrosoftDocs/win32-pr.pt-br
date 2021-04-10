---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 7 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo de ação personalizada 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011157"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="c884c-103">Tipo de ação personalizada 7</span><span class="sxs-lookup"><span data-stu-id="c884c-103">Custom Action Type 7</span></span>

<span data-ttu-id="c884c-104">O tipo de ação personalizada 7 é usado com instalações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c884c-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="c884c-105">As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público.</span><span class="sxs-lookup"><span data-stu-id="c884c-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="c884c-106">Para obter mais informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="c884c-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="c884c-107">Essa ação personalizada instala outro pacote do instalador que está aninhado dentro do primeiro pacote.</span><span class="sxs-lookup"><span data-stu-id="c884c-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="c884c-108">Fonte</span><span class="sxs-lookup"><span data-stu-id="c884c-108">Source</span></span>

<span data-ttu-id="c884c-109">O banco de dados do aplicativo simultâneo é armazenado como um subarmazenamento do pacote e o nome do subarmazenamento é designado no campo de origem da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="c884c-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="c884c-110">Tipo numérico</span><span class="sxs-lookup"><span data-stu-id="c884c-110">Numeric Type</span></span>



| <span data-ttu-id="c884c-111">Nome do tipo</span><span class="sxs-lookup"><span data-stu-id="c884c-111">Type name</span></span>                                                      | <span data-ttu-id="c884c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c884c-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="c884c-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span><span class="sxs-lookup"><span data-stu-id="c884c-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="c884c-114">7</span><span class="sxs-lookup"><span data-stu-id="c884c-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="c884c-115">Destino</span><span class="sxs-lookup"><span data-stu-id="c884c-115">Target</span></span>

<span data-ttu-id="c884c-116">O campo de destino da [tabela CustomAction](customaction-table.md) contém configurações de propriedade a serem passadas para a instalação simultânea.</span><span class="sxs-lookup"><span data-stu-id="c884c-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="c884c-117">Essas configurações de propriedade podem especificar recursos.</span><span class="sxs-lookup"><span data-stu-id="c884c-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="c884c-118">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="c884c-118">Return Processing Options</span></span>

<span data-ttu-id="c884c-119">A sessão de instalação simultânea é executada como um thread separado no processo atual.</span><span class="sxs-lookup"><span data-stu-id="c884c-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="c884c-120">Uma instalação simultânea não pode ser executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c884c-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="c884c-121">Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="c884c-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="c884c-122">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="c884c-122">Execution Scheduling Options</span></span>

<span data-ttu-id="c884c-123">Sinalizadores de opções estão disponíveis para controlar a possível execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c884c-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="c884c-124">Consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="c884c-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="c884c-125">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="c884c-125">In-Script Execution Options</span></span>

<span data-ttu-id="c884c-126">Essa ação personalizada não usa essa opção.</span><span class="sxs-lookup"><span data-stu-id="c884c-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="c884c-127">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c884c-127">Return Values</span></span>

<span data-ttu-id="c884c-128">O status de retorno da saída do usuário, falha, suspensão ou êxito de uma instalação simultânea é processado da mesma maneira que qualquer outra ação.</span><span class="sxs-lookup"><span data-stu-id="c884c-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="c884c-129">No entanto, observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="c884c-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="c884c-130">Por exemplo, se o valor de retorno da ação aparecer como 1 no arquivo de log, isso significa que a ação retornou êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="c884c-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="c884c-131">Para obter mais informações sobre essa conversão, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c884c-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="c884c-132">Observe que, se uma instalação simultânea tiver **msidbCustomActionTypeContinue** definido, um retorno de erro \_ instalar o \_ UserExit, erro de \_ instalação \_ reinicializar, erro de \_ instalação \_ reinicializar \_ agora ou \_ \_ a reinicialização de êxito de erro \_ necessária é tratada como êxito do erro \_ .</span><span class="sxs-lookup"><span data-stu-id="c884c-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="c884c-133">Isso significa que, se você definir **msidbCustomActionTypeContinue** e sua instalação simultânea exigir uma reinicialização, o requisito para a reinicialização será ignorado.</span><span class="sxs-lookup"><span data-stu-id="c884c-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="c884c-134">Além disso, o código de erro da ação personalizada de instalação simultânea será ignorado.</span><span class="sxs-lookup"><span data-stu-id="c884c-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="c884c-135">Se **msidbCustomActionTypeContinue** não for definido, os códigos de retorno a seguir mais o sucesso do erro \_ serão tratados como sucesso e terão os seguintes significados.</span><span class="sxs-lookup"><span data-stu-id="c884c-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="c884c-136">Outros códigos de retorno são tratados como falha.</span><span class="sxs-lookup"><span data-stu-id="c884c-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="c884c-137">Mensagem</span><span class="sxs-lookup"><span data-stu-id="c884c-137">Message</span></span>                          | <span data-ttu-id="c884c-138">Significado</span><span class="sxs-lookup"><span data-stu-id="c884c-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c884c-139">ERRO ao \_ instalar a \_ reinicialização</span><span class="sxs-lookup"><span data-stu-id="c884c-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="c884c-140">O sinalizador de reinicialização será definido para reiniciar no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="c884c-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="c884c-141">ERRO ao \_ instalar \_ reinicializar \_ agora</span><span class="sxs-lookup"><span data-stu-id="c884c-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="c884c-142">Uma reinicialização é necessária antes de concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="c884c-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="c884c-143">A reinicialização será processada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c884c-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="c884c-144">ERRO \_ de \_ reinicialização bem-sucedida \_ necessária</span><span class="sxs-lookup"><span data-stu-id="c884c-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="c884c-145">Uma reinicialização era necessária, mas foi suprimida.</span><span class="sxs-lookup"><span data-stu-id="c884c-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="c884c-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="c884c-146">Remarks</span></span>

<span data-ttu-id="c884c-147">Uma expressão condicional é necessária para habilitar a instalação simultânea em qualquer instalação ou remoção do componente ou recurso associado.</span><span class="sxs-lookup"><span data-stu-id="c884c-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c884c-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c884c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c884c-149">Instalações simultâneas</span><span class="sxs-lookup"><span data-stu-id="c884c-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="c884c-150">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="c884c-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="c884c-151">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c884c-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c884c-152">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="c884c-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="c884c-153">Valores de retorno de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="c884c-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



