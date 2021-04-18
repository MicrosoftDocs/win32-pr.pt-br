---
description: Um aplicativo COM+ é essencialmente um Construtor declarativo que permite que você configure qualquer número de componentes em comum. Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789262"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="8302b-104">Configurando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="8302b-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="8302b-105">Um aplicativo COM+ é essencialmente um Construtor declarativo que permite que você configure qualquer número de componentes em comum.</span><span class="sxs-lookup"><span data-stu-id="8302b-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="8302b-106">Por exemplo, você pode configurar os componentes em um aplicativo com uma política de segurança comum.</span><span class="sxs-lookup"><span data-stu-id="8302b-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="8302b-107">A configuração é uma parte essencial do processo de desenvolvimento para aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="8302b-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="8302b-108">A maneira como você configura um aplicativo determinará como o COM+ fornecerá serviços para ele e como ele se comporta durante a execução.</span><span class="sxs-lookup"><span data-stu-id="8302b-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="8302b-109">Você pode configurar aplicativos COM+ usando a ferramenta de administração de serviços de componentes ou os objetos e as interfaces de administração programáveis que fornecem a funcionalidade subjacente da ferramenta de administração.</span><span class="sxs-lookup"><span data-stu-id="8302b-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="8302b-110">Para obter detalhes sobre como executar a administração com script, consulte [automatizando a administração do com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="8302b-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="8302b-111">Você pode configurar elementos nos seguintes níveis em aplicativos COM+:</span><span class="sxs-lookup"><span data-stu-id="8302b-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="8302b-112">Configurações de nível de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8302b-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="8302b-113">Configurações de nível de componente (nível de classe)</span><span class="sxs-lookup"><span data-stu-id="8302b-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="8302b-114">Configuração de nível de interface</span><span class="sxs-lookup"><span data-stu-id="8302b-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="8302b-115">Configuração de nível de método</span><span class="sxs-lookup"><span data-stu-id="8302b-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="8302b-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8302b-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="8302b-117">A maneira como você instala componentes em um aplicativo pode afetar como você pode configurá-los.</span><span class="sxs-lookup"><span data-stu-id="8302b-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="8302b-118">Você sempre deve instalar componentes em aplicativos COM+ (em vez de importá-los).</span><span class="sxs-lookup"><span data-stu-id="8302b-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="8302b-119">A instalação de componentes irá registrá-los totalmente, juntamente com interfaces e bibliotecas de tipos, no banco de dados de registro de classe COM+ (RegDB) para que você possa configurá-los.</span><span class="sxs-lookup"><span data-stu-id="8302b-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="8302b-120">Configurações de Application-Level</span><span class="sxs-lookup"><span data-stu-id="8302b-120">Application-Level Settings</span></span>



| <span data-ttu-id="8302b-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="8302b-121">Attribute</span></span>                                                                                        | <span data-ttu-id="8302b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8302b-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8302b-123">Ativação</span><span class="sxs-lookup"><span data-stu-id="8302b-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="8302b-124">Especifica o tipo de aplicativo: servidor de aplicativos ou aplicativo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8302b-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="8302b-125">Habilitando verificações de acesso</span><span class="sxs-lookup"><span data-stu-id="8302b-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="8302b-126">Ativa e desativa a verificação de segurança.</span><span class="sxs-lookup"><span data-stu-id="8302b-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="8302b-127">Nível de segurança</span><span class="sxs-lookup"><span data-stu-id="8302b-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="8302b-128">Especifica que as verificações de acesso serão executadas no nível do processo (níveis de verificação de acesso gerados a partir de funções) ou no processo e em níveis de componente (segurança baseada em função completa).</span><span class="sxs-lookup"><span data-stu-id="8302b-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="8302b-129">Nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="8302b-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="8302b-130">Define o nível de autenticação usado em chamadas para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8302b-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="8302b-131">Nível de representação</span><span class="sxs-lookup"><span data-stu-id="8302b-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="8302b-132">Define o nível de representação usado em chamadas para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8302b-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="8302b-133">Serviço</span><span class="sxs-lookup"><span data-stu-id="8302b-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="8302b-134">Especifica que os componentes de aplicativo usarão serviços de enfileiramento.</span><span class="sxs-lookup"><span data-stu-id="8302b-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="8302b-135">Habilitar CRM</span><span class="sxs-lookup"><span data-stu-id="8302b-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="8302b-136">Habilita o uso de gerenciadores de recursos de compensação.</span><span class="sxs-lookup"><span data-stu-id="8302b-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="8302b-137">Executar aplicativo como serviço</span><span class="sxs-lookup"><span data-stu-id="8302b-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="8302b-138">Configura e implementa um aplicativo de servidor COM+ como um serviço NT.</span><span class="sxs-lookup"><span data-stu-id="8302b-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8302b-139">Serviço SOAP COM+</span><span class="sxs-lookup"><span data-stu-id="8302b-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="8302b-140">Expõe um aplicativo COM+ como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="8302b-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="8302b-141">Pool de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8302b-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="8302b-142">Adiciona escalabilidade para processos de thread único e integra-se com o serviço de reciclagem de aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="8302b-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="8302b-143">Reciclagem de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8302b-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="8302b-144">Aumenta a estabilidade do aplicativo, desligando um processo associado a um aplicativo e reiniciando-o.</span><span class="sxs-lookup"><span data-stu-id="8302b-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="8302b-145">Despejo de processo</span><span class="sxs-lookup"><span data-stu-id="8302b-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="8302b-146">Despeja o estado inteiro de um processo sem encerrá-lo, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="8302b-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="8302b-147">Desligamento de processo do servidor</span><span class="sxs-lookup"><span data-stu-id="8302b-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="8302b-148">Desliga um processo após um período ocioso especificado.</span><span class="sxs-lookup"><span data-stu-id="8302b-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="8302b-149">Permissões</span><span class="sxs-lookup"><span data-stu-id="8302b-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="8302b-150">Desabilita as alterações nas definições de configuração, incluindo a exclusão.</span><span class="sxs-lookup"><span data-stu-id="8302b-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="8302b-151">Identidade de segurança</span><span class="sxs-lookup"><span data-stu-id="8302b-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="8302b-152">Especifica a identidade sob a qual o aplicativo é executado.</span><span class="sxs-lookup"><span data-stu-id="8302b-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="8302b-153">Iniciar no depurador</span><span class="sxs-lookup"><span data-stu-id="8302b-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="8302b-154">Especifica que o aplicativo será iniciado em um depurador, com as configurações de linha de comando especificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8302b-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="8302b-155">Habilitar suporte a 3GB</span><span class="sxs-lookup"><span data-stu-id="8302b-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="8302b-156">Habilita o uso do espaço de endereço de memória de processo estendido.</span><span class="sxs-lookup"><span data-stu-id="8302b-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="8302b-157">Configurações de Component-Level (nível de classe)</span><span class="sxs-lookup"><span data-stu-id="8302b-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8302b-158">Atributo</span><span class="sxs-lookup"><span data-stu-id="8302b-158">Attribute</span></span></th>
<th><span data-ttu-id="8302b-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="8302b-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8302b-160"><a href="configuring-transactions.md">Transações</a></span><span class="sxs-lookup"><span data-stu-id="8302b-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="8302b-161">Define os requisitos automáticos de transação desabilitados, sem suporte, com suporte, necessários ou requer novos.</span><span class="sxs-lookup"><span data-stu-id="8302b-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8302b-162"><a href="setting-the-synchronization-attribute.md">Sincronização</a></span><span class="sxs-lookup"><span data-stu-id="8302b-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="8302b-163">Define os requisitos de sincronização desabilitados, sem suporte, com suporte, obrigatório ou requer novos.</span><span class="sxs-lookup"><span data-stu-id="8302b-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8302b-164"><a href="enabling-jit-activation-for-a-component.md">Ativação JIT</a></span><span class="sxs-lookup"><span data-stu-id="8302b-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="8302b-165">Habilita a ativação Just-in-time.</span><span class="sxs-lookup"><span data-stu-id="8302b-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8302b-166"><a href="configuring-a-component-to-be-pooled.md">Pool de objetos</a></span><span class="sxs-lookup"><span data-stu-id="8302b-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="8302b-167">Habilita o pooling de objetos.</span><span class="sxs-lookup"><span data-stu-id="8302b-167">Enables object pooling.</span></span> <span data-ttu-id="8302b-168">O tamanho mínimo e máximo do pool e os valores de tempo limite do objeto são configuráveis.</span><span class="sxs-lookup"><span data-stu-id="8302b-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8302b-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Construção de objeto</a></span><span class="sxs-lookup"><span data-stu-id="8302b-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="8302b-170">Habilita a construção de objeto com parâmetros com uma cadeia de caracteres de Construtor especificada administrativamente.</span><span class="sxs-lookup"><span data-stu-id="8302b-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8302b-171">A cadeia de caracteres do construtor não deve ser usada para armazenar informações confidenciais de segurança.</span><span class="sxs-lookup"><span data-stu-id="8302b-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8302b-172"><a href="enabling-access-checks-at-the-component-level.md">Verificações de acesso no nível do componente</a></span><span class="sxs-lookup"><span data-stu-id="8302b-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="8302b-173">Ativa ou desativa a verificação de segurança baseada em função no nível de componente.</span><span class="sxs-lookup"><span data-stu-id="8302b-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8302b-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Atribuição de função declarativa</a></span><span class="sxs-lookup"><span data-stu-id="8302b-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="8302b-175">Habilita a atribuição explícita de funções ao componente.</span><span class="sxs-lookup"><span data-stu-id="8302b-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8302b-176"><a href="persistent-client-side-failures.md">Classe de exceção de enfileiramento</a></span><span class="sxs-lookup"><span data-stu-id="8302b-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="8302b-177">Indica uma classe de exceção para lidar com falhas do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="8302b-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8302b-178"><a href="com--instrumentation-concepts.md">Eventos de instrumentação e estatísticas</a></span><span class="sxs-lookup"><span data-stu-id="8302b-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="8302b-179">Habilita o relatório detalhado de eventos do sistema e estatísticas de objeto.</span><span class="sxs-lookup"><span data-stu-id="8302b-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8302b-180"><a href="context-activation.md">Contexto de ativação</a></span><span class="sxs-lookup"><span data-stu-id="8302b-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="8302b-181">Habilita a ativação forçada de um objeto no contexto do chamador ou no contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="8302b-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8302b-182"><a href="what-s-new-in-com--1-5.md">Criando componentes privados</a></span><span class="sxs-lookup"><span data-stu-id="8302b-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="8302b-183">Marca o componente como privado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8302b-183">Marks component as private to the application.</span></span> <span data-ttu-id="8302b-184">Um componente privado pode ser visto e ativado somente por outros componentes no mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8302b-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="8302b-185">Interface-Level configuração</span><span class="sxs-lookup"><span data-stu-id="8302b-185">Interface-Level Setting</span></span>



| <span data-ttu-id="8302b-186">Atributo</span><span class="sxs-lookup"><span data-stu-id="8302b-186">Attribute</span></span>                                                                                           | <span data-ttu-id="8302b-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="8302b-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8302b-188">Em fila</span><span class="sxs-lookup"><span data-stu-id="8302b-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="8302b-189">Indica uma interface queuable, definida em IDL.</span><span class="sxs-lookup"><span data-stu-id="8302b-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="8302b-190">Atribuição de função declarativa</span><span class="sxs-lookup"><span data-stu-id="8302b-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="8302b-191">Habilita a atribuição explícita de funções à interface, bem como funções herdadas implicitamente do nível de componente.</span><span class="sxs-lookup"><span data-stu-id="8302b-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="8302b-192">Method-Level configuração</span><span class="sxs-lookup"><span data-stu-id="8302b-192">Method-Level Setting</span></span>



| <span data-ttu-id="8302b-193">Atributo</span><span class="sxs-lookup"><span data-stu-id="8302b-193">Attribute</span></span>                                                                                           | <span data-ttu-id="8302b-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="8302b-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8302b-195">Concluído automaticamente</span><span class="sxs-lookup"><span data-stu-id="8302b-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="8302b-196">Desativa automaticamente o objeto no retorno do método e nos votos na transação.</span><span class="sxs-lookup"><span data-stu-id="8302b-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="8302b-197">Atribuição de função declarativa</span><span class="sxs-lookup"><span data-stu-id="8302b-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="8302b-198">Habilita a atribuição explícita de funções para o método, bem como funções herdadas implicitamente dos níveis de interface e componente.</span><span class="sxs-lookup"><span data-stu-id="8302b-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8302b-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8302b-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8302b-200">Automatizando a administração do COM+</span><span class="sxs-lookup"><span data-stu-id="8302b-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="8302b-201">Criando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="8302b-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="8302b-202">Implantando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="8302b-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




