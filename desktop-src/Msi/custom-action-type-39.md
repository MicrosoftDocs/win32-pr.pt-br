---
description: Os desenvolvedores de Windows Installer pacotes podem optar por usar um tipo de ação personalizada 39 quando as ações padrão são insuficientes para executar a instalação.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo de ação personalizada 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828875"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="5f46d-103">Tipo de ação personalizada 39</span><span class="sxs-lookup"><span data-stu-id="5f46d-103">Custom Action Type 39</span></span>

<span data-ttu-id="5f46d-104">O tipo de ação personalizada 39 é usado com instalações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5f46d-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="5f46d-105">As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público.</span><span class="sxs-lookup"><span data-stu-id="5f46d-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="5f46d-106">Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="5f46d-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="5f46d-107">Digite 39 ação personalizada instala um aplicativo que é anunciado ou já instalado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="5f46d-108">Esse tipo de ação personalizada pode ser usado para reinstalar ou remover um produto que foi instalado como uma instalação simultânea pelo pacote de instalação do produto atual.</span><span class="sxs-lookup"><span data-stu-id="5f46d-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="5f46d-109">O tipo 39 ação personalizada não pode ser usado para reinstalar ou remover qualquer produto instalado anteriormente por outros meios.</span><span class="sxs-lookup"><span data-stu-id="5f46d-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="5f46d-110">Por exemplo, se o produto secundário for instalado usando um tipo 39, tipo 23 ou ação personalizada do tipo 7 durante a instalação do produto principal, uma ação personalizada de tipo 39 poderá ser usada para remover o produto secundário quando o produto primário for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="5f46d-111">Fonte</span><span class="sxs-lookup"><span data-stu-id="5f46d-111">Source</span></span>

<span data-ttu-id="5f46d-112">O campo origem da [tabela CustomAction](customaction-table.md) contém o código do produto para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f46d-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="5f46d-113">Tipo numérico</span><span class="sxs-lookup"><span data-stu-id="5f46d-113">Numeric Type</span></span>



| <span data-ttu-id="5f46d-114">Nome do tipo</span><span class="sxs-lookup"><span data-stu-id="5f46d-114">Type name</span></span>                                                     | <span data-ttu-id="5f46d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5f46d-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="5f46d-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span><span class="sxs-lookup"><span data-stu-id="5f46d-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="5f46d-117">39</span><span class="sxs-lookup"><span data-stu-id="5f46d-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="5f46d-118">Destino</span><span class="sxs-lookup"><span data-stu-id="5f46d-118">Target</span></span>

<span data-ttu-id="5f46d-119">O campo de destino da [tabela CustomAction](customaction-table.md) contém configurações de propriedade que devem ser passadas para a instalação simultânea.</span><span class="sxs-lookup"><span data-stu-id="5f46d-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="5f46d-120">Essas configurações de propriedade podem especificar recursos.</span><span class="sxs-lookup"><span data-stu-id="5f46d-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="5f46d-121">Opções de processamento de retorno</span><span class="sxs-lookup"><span data-stu-id="5f46d-121">Return Processing Options</span></span>

<span data-ttu-id="5f46d-122">O tipo de ação personalizada 39 falhará se o aplicativo não for anunciado ou instalado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="5f46d-123">Para evitar essa falha, você deve definir o **msidbCustomActionTypeContinueflag**.</span><span class="sxs-lookup"><span data-stu-id="5f46d-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="5f46d-124">Uma instalação simultânea não pode ser executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5f46d-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="5f46d-125">Consulte [Opções de processamento de retorno de ação personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="5f46d-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="5f46d-126">Opções de agendamento de execução</span><span class="sxs-lookup"><span data-stu-id="5f46d-126">Execution Scheduling Options</span></span>

<span data-ttu-id="5f46d-127">Sinalizadores de opções estão disponíveis para controlar a possível execução de várias ações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="5f46d-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="5f46d-128">Consulte [Opções de agendamento de execução de ação personalizada](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="5f46d-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="5f46d-129">Opções de execução de In-Script</span><span class="sxs-lookup"><span data-stu-id="5f46d-129">In-Script Execution Options</span></span>

<span data-ttu-id="5f46d-130">A ação personalizada não usa essa opção.</span><span class="sxs-lookup"><span data-stu-id="5f46d-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f46d-131">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5f46d-131">Return Values</span></span>

<span data-ttu-id="5f46d-132">O status de retorno da saída do usuário, falha, suspensão ou êxito de uma instalação simultânea é processado da mesma maneira que qualquer outra ação.</span><span class="sxs-lookup"><span data-stu-id="5f46d-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="5f46d-133">No entanto, observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="5f46d-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="5f46d-134">Por exemplo, se o valor de retorno da ação aparecer como 1 no arquivo de log, isso significa que a ação retornou êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="5f46d-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="5f46d-135">Para obter mais informações, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5f46d-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="5f46d-136">Observe que, se uma instalação simultânea tiver **msidbCustomActionTypeContinue** definido, um retorno de erro \_ instalar o \_ usersair, erro de \_ instalação \_ reinicializar, erro de \_ instalação \_ inicial \_ agora ou \_ reinicialização de êxito de erro \_ \_ necessária é tratada como êxito de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="5f46d-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="5f46d-137">Isso significa que, se você definir **msidbCustomActionTypeContinue** e sua instalação simultânea exigir uma reinicialização, o requisito para a reinicialização será ignorado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="5f46d-138">Além disso, o código de erro da ação personalizada de instalação simultânea será ignorado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="5f46d-139">Se **msidbCustomActionTypeContinue** não for definido, os códigos de retorno a seguir mais o sucesso do erro \_ serão tratados como sucesso e terão os seguintes significados.</span><span class="sxs-lookup"><span data-stu-id="5f46d-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="5f46d-140">Outros códigos de retorno são tratados como falha.</span><span class="sxs-lookup"><span data-stu-id="5f46d-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="5f46d-141">Mensagem</span><span class="sxs-lookup"><span data-stu-id="5f46d-141">Message</span></span>                          | <span data-ttu-id="5f46d-142">Significado</span><span class="sxs-lookup"><span data-stu-id="5f46d-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f46d-143">ERRO ao \_ instalar a \_ reinicialização</span><span class="sxs-lookup"><span data-stu-id="5f46d-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="5f46d-144">O sinalizador de reinicialização será definido para reiniciar no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="5f46d-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="5f46d-145">ERRO ao \_ instalar \_ reinicializar \_ agora</span><span class="sxs-lookup"><span data-stu-id="5f46d-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="5f46d-146">Uma reinicialização é necessária antes de concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="5f46d-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="5f46d-147">A reinicialização será processada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5f46d-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="5f46d-148">ERRO \_ de \_ reinicialização bem-sucedida \_ necessária</span><span class="sxs-lookup"><span data-stu-id="5f46d-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="5f46d-149">Uma reinicialização era necessária, mas foi suprimida.</span><span class="sxs-lookup"><span data-stu-id="5f46d-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5f46d-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f46d-150">Remarks</span></span>

<span data-ttu-id="5f46d-151">Uma expressão condicional é necessária para habilitar a instalação simultânea em qualquer instalação ou remoção do componente ou recurso associado.</span><span class="sxs-lookup"><span data-stu-id="5f46d-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f46d-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f46d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f46d-153">Instalações simultâneas</span><span class="sxs-lookup"><span data-stu-id="5f46d-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="5f46d-154">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="5f46d-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="5f46d-155">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="5f46d-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="5f46d-156">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="5f46d-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



