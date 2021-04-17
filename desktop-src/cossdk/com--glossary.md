---
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26a72de1-24bc-41e6-8d41-61d45f581e51
title: Glossário do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b5a6cb30529cd8b97b8cf11316347d68003e32c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456984"
---
# <a name="com-glossary"></a><span data-ttu-id="3aa2c-103">Glossário do COM+</span><span class="sxs-lookup"><span data-stu-id="3aa2c-103">COM+ Glossary</span></span>

<dl> <dt>

<span data-ttu-id="3aa2c-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**token de acesso**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-104"><span id="cos.access_token_gloss"></span><span id="COS.ACCESS_TOKEN_GLOSS"></span>**access token**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-105">Um objeto que descreve o contexto de segurança de um processo ou thread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-105">An object that describes the security context of a process or thread.</span></span> <span data-ttu-id="3aa2c-106">As informações em um token incluem a identidade e os privilégios da conta de usuário associada ao processo ou thread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-106">The information in a token includes the identity and privileges of the user account associated with the process or thread.</span></span> <span data-ttu-id="3aa2c-107">Quando um usuário faz logon, o sistema verifica a senha do usuário comparando-a com as informações armazenadas em um banco de dados de segurança.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-107">When a user logs on, the system verifies the user's password by comparing it with information stored in a security database.</span></span> <span data-ttu-id="3aa2c-108">Se a senha for autenticada, o sistema produzirá um token de acesso.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-108">If the password is authenticated, the system produces an access token.</span></span> <span data-ttu-id="3aa2c-109">Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-109">Every process executed on behalf of this user has a copy of this access token.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**Propriedades ACID**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-110"><span id="cos.acid_properties_gloss"></span><span id="COS.ACID_PROPERTIES_GLOSS"></span>**ACID properties**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-111">Acrônimo cunhado pelos pioneiros de processamento de transações para Atomic, consistente, isolado e durável.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-111">Acronym coined by transaction processing pioneers for atomic, consistent, isolated, and durable.</span></span> <span data-ttu-id="3aa2c-112">Essas propriedades garantem um comportamento previsível, reforçando a função de transações como todas as proposições de tudo ou nenhum projetadas para fornecer resultados consistentes e previsíveis em um ambiente distribuído quando podem ocorrer falhas independentes.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-112">These properties ensure predictable behavior, reinforcing the role of transactions as all-or-none propositions designed to provide consistent and predictable results in a distributed environment when independent failures can occur.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**ativá**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-113"><span id="cos.activation_gloss"></span><span id="COS.ACTIVATION_GLOSS"></span>**activation**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-114">A cadeia de eventos que resulta na criação de um objeto COM e o retorno de um ponteiro válido para uma interface nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-114">The chain of events that results in the creation of a COM object and the return of a valid pointer to an interface on that object.</span></span> <span data-ttu-id="3aa2c-115">No COM+, um objeto é ativado em seu próprio contexto ou no seu criador (um objeto que solicitou o objeto que está sendo ativado).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-115">In COM+, an object gets activated either in its own context or in that of its creator (an object that has requested the object being activated).</span></span> <span data-ttu-id="3aa2c-116">Os serviços COM+ dependem da ativação apropriada de um objeto com base na configuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-116">COM+ services rely on appropriate activation of an object based on the object's configuration.</span></span> <span data-ttu-id="3aa2c-117">No decorrer da ativação, o sistema determina o contexto no qual o objeto é executado, inicializa as propriedades de contexto, verifica as permissões de acesso e estabelece uma identidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-117">In the course of activation, the system determines the context in which the object runs, initializes the context properties, checks access permissions, and establishes a security identity.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**segurança de ativação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-118"><span id="cos.activation_security_gloss"></span><span id="COS.ACTIVATION_SECURITY_GLOSS"></span>**activation security**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-119">Uma forma de proteção de segurança que determina quem pode iniciar um servidor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-119">A form of security protection that determines who can launch a server.</span></span> <span data-ttu-id="3aa2c-120">A segurança de ativação é aplicada automaticamente pelo SCM (Gerenciador de controle de serviço) de um computador específico.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-120">Activation security is automatically applied by the Service Control Manager (SCM) of a particular computer.</span></span> <span data-ttu-id="3aa2c-121">Após o recebimento de uma solicitação de um cliente para ativar um objeto, o SCM verifica a solicitação de informações de segurança de ativação armazenadas em seu registro.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-121">Upon receipt of a request from a client to activate an object, the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="3aa2c-122">A segurança de ativação também é verificada quanto a ativações de mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-122">Activation security is also checked for same-computer activations.</span></span> <span data-ttu-id="3aa2c-123">Também chamado de *segurança de inicialização*.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-123">Also called *launch security*.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**tipo de ativação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-124"><span id="cos.activation_type_gloss"></span><span id="COS.ACTIVATION_TYPE_GLOSS"></span>**activation type**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-125">Categoria de ativação para um aplicativo COM+ que indica se o aplicativo é executado dentro ou fora do espaço de processo do cliente (dependendo se é um aplicativo de biblioteca ou de servidor, respectivamente), bem como se o aplicativo é executado como um serviço.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-125">Activation category for a COM+ application that indicates whether the application runs in or out of its client's process space (depending on whether it's a library or server application, respectively) as well as whether the application runs as a service.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**actividade**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-126"><span id="cos.activity_gloss"></span><span id="COS.ACTIVITY_GLOSS"></span>**activity**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-127">No COM+, um thread lógico que compreende uma ou mais transações e que contém uma coleção de componentes que são agrupados em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-127">In COM+, a logical thread comprising one or more transactions and containing a collection of components that are grouped into a COM+ application.</span></span> <span data-ttu-id="3aa2c-128">Cada objeto COM pertence a uma atividade.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-128">Every COM object belongs to one activity.</span></span> <span data-ttu-id="3aa2c-129">A associação entre um objeto e uma atividade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-129">The association between an object and an activity cannot be changed.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**processo de modelo de apartamento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-130"><span id="cos.apartment_model_process_gloss"></span><span id="COS.APARTMENT_MODEL_PROCESS_GLOSS"></span>**apartment model process**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-131">Um processo que tem dois ou mais Apartments de thread único e nenhum Apartments multithread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-131">A process that has two or more single-threaded apartments and no multithreaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**proxy de aplicativo**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-132"><span id="cos.application_proxy_gloss"></span><span id="COS.APPLICATION_PROXY_GLOSS"></span>**application proxy**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-133">Um conjunto de arquivos que contém informações de registro que permitem que um cliente acesse remotamente um aplicativo de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-133">A set of files containing registration information that allows a client to remotely access a COM+ server application.</span></span> <span data-ttu-id="3aa2c-134">Quando instalado em um computador cliente, um arquivo de proxy de aplicativo grava informações sobre o aplicativo de servidor no computador cliente; o cliente pode acessar remotamente o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-134">When installed on a client computer, an application proxy file writes information about the server application to the client computer; the client can then remotely access the server application.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**Authentication**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-135"><span id="cos.authentication_gloss"></span><span id="COS.AUTHENTICATION_GLOSS"></span>**authentication**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-136">O processo de segurança de determinar que um chamador de um aplicativo realmente diz que ele é, verificando a autenticidade de uma declaração de identidade.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-136">The security process of determining that a caller of an application is actually who it says it is—verifying the authenticity of an identity claim.</span></span> <span data-ttu-id="3aa2c-137">Para aplicativos COM+, a autenticação pode ser ativada e configurada administrativamente, após a qual ela funciona de forma transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-137">For COM+ applications, authentication can be turned on and configured administratively, after which it works transparently to the application.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**nesse**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-138"><span id="cos.authorization_gloss"></span><span id="COS.AUTHORIZATION_GLOSS"></span>**authorization**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-139">O processo de segurança de determinar se um chamador de um aplicativo está autorizado a fazer o que ele está pedindo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-139">The security process of determining whether a caller of an application is authorized to do what it is asking to do.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos de caching**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-140"><span id="cos.caching_resource_manager_gloss"></span><span id="COS.CACHING_RESOURCE_MANAGER_GLOSS"></span>**caching resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-141">Um Gerenciador de recursos que atua como um front-end para outro gerenciador de recursos e que armazena em cache as informações localmente, reduzindo o custo de acesso ao recurso subjacente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-141">A resource manager that acts as a front-end to another resource manager and that caches information locally, reducing the cost of accessing the underlying resource.</span></span> <span data-ttu-id="3aa2c-142">Ao contrário de um Gerenciador de recursos convencional, um Gerenciador de recursos de cache não participa da recuperação porque nunca armazena permanentemente os dados subjacentes.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-142">Unlike a conventional resource manager, a caching resource manager does not participate in recovery because it never permanently stores the underlying data.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**chamar segurança**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-143"><span id="cos.call_security_gloss"></span><span id="COS.CALL_SECURITY_GLOSS"></span>**call security**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-144">Uma forma de proteção de segurança que ajuda a controlar o acesso a métodos de um objeto de servidor depois que um servidor é iniciado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-144">A form of security protection that helps control access to a server object's methods after a server has been launched.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**classe (COM)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-145"><span id="cos.class_gloss"></span><span id="COS.CLASS_GLOSS"></span>**class (COM)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-146">Uma implementação nomeada e concreta de uma ou mais interfaces.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-146">A named, concrete implementation of one or more interfaces.</span></span> <span data-ttu-id="3aa2c-147">Uma classe COM é identificada por um CLSID e, às vezes, de um ProgID.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-147">A COM class is identified by a CLSID and, sometimes, a ProgID.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**encobrimento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-148"><span id="cos.cloaking_gloss"></span><span id="COS.CLOAKING_GLOSS"></span>**cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-149">A capacidade do servidor de mascarar sua própria identidade ao fazer chamadas em nome de um cliente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-149">A server's ability to mask its own identity when making calls on a client's behalf.</span></span> <span data-ttu-id="3aa2c-150">Quando o encobrimento está habilitado, as chamadas feitas pelo servidor representando o cliente podem ser feitas sob a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-150">When cloaking is enabled, calls made by the server impersonating the client can be made under the client's identity.</span></span> <span data-ttu-id="3aa2c-151">Quando o encobrimento estiver desabilitado, as chamadas pelo servidor serão feitas sob a identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-151">When cloaking is disabled, calls by the server will be made under the server's identity.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**Aplicativo COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-152"><span id="cos.complus_application_gloss"></span><span id="COS.COMPLUS_APPLICATION_GLOSS"></span>**COM+ application**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-153">A unidade primária de administração e segurança para serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-153">The primary unit of administration and security for Component Services.</span></span> <span data-ttu-id="3aa2c-154">Um aplicativo COM+ é um grupo de componentes COM que, em geral, executam funções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-154">A COM+ application is a group of COM components that, generally, perform related functions.</span></span> <span data-ttu-id="3aa2c-155">Esses componentes consistem mais em interfaces e métodos COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-155">These components further consist of COM interfaces and methods.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**Pool de aplicativos COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-156"><span id="cos.complus_application_pooling_gloss"></span><span id="COS.COMPLUS_APPLICATION_POOLING_GLOSS"></span>**COM+ Application Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-157">Um recurso dos serviços de componentes que permite a escala de processos single-thread e também pode ajudá-lo a se recuperar de falhas em processos únicos, fornecendo outros processos em execução capazes de lidar com ativações.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-157">A Component Services feature that allows single-threaded processes to scale and can also help you recover from failures in single processes by providing other running processes able to handle activations.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**Reciclagem de aplicativos COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-158"><span id="cos.complus_application_recycling_gloss"></span><span id="COS.COMPLUS_APPLICATION_RECYCLING_GLOSS"></span>**COM+ Application Recycling**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-159">Um recurso dos serviços de componentes que aumenta significativamente a estabilidade geral de seus aplicativos, permitindo que você desligue normalmente um processo associado a um aplicativo e reinicie-o.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-159">A Component Services feature that significantly increases the overall stability of your applications by allowing you to gracefully shut down a process associated with an application and restart it.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**Catálogo COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-160"><span id="cos.complus_catalog_gloss"></span><span id="COS.COMPLUS_CATALOG_GLOSS"></span>**COM+ catalog**</span></span> 
</dt> <dd>

<span data-ttu-id="3aa2c-161">O armazenamento de dados que contém dados de configuração do COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-161">The data store that holds COM+ configuration data.</span></span> <span data-ttu-id="3aa2c-162">O desempenho das tarefas de administração do COM+ requer a leitura e a gravação de dados armazenados no catálogo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-162">Performance of COM+ administration tasks requires reading and writing data stored in the catalog.</span></span> <span data-ttu-id="3aa2c-163">O catálogo pode ser acessado somente por meio da ferramenta administrativa serviços de componentes ou da biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-163">The catalog can be accessed only through the Component Services administrative tool or through the COMAdmin library.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**Eventos COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-164"><span id="cos.complus_events_gloss"></span><span id="COS.COMPLUS_EVENTS_GLOSS"></span>**COM+ Events**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-165">Os eventos COM+ correspondem e conecta editores e assinantes por meio de um sistema de eventos livremente acoplado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-165">COM+ Events matches and connects publishers and subscribers through a loosely coupled events system.</span></span> <span data-ttu-id="3aa2c-166">Um Publicador faz a chamada de método para iniciar um evento e um assinante recebe essas chamadas por meio do sistema de eventos, e não diretamente do Publicador.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-166">A publisher makes the method call to initiate an event, and a subscriber receives these calls through the event system rather than directly from the publisher.</span></span> <span data-ttu-id="3aa2c-167">O serviço de eventos COM+ mantém a lista de assinantes interessados que recebem as chamadas e direciona essas chamadas sem a necessidade do conhecimento do Publicador.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-167">The COM+ Events service maintains the list of interested subscribers who receive the calls and directs those calls without requiring the knowledge of the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**Aplicativo de biblioteca COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-168"><span id="cos.complus_library_application_gloss"></span><span id="COS.COMPLUS_LIBRARY_APPLICATION_GLOSS"></span>**COM+ library application**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-169">Um aplicativo COM+ que é executado no processo do cliente que o cria.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-169">A COM+ application that runs in the process of the client that creates it.</span></span> <span data-ttu-id="3aa2c-170">Os aplicativos de biblioteca podem usar a segurança baseada em função, mas não dão suporte a acesso remoto ou a componentes na fila.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-170">Library applications can use role-based security but do not support remote access or queued components.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**Pool de objetos COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-171"><span id="cos.complus_object_pooling_gloss"></span><span id="COS.COMPLUS_OBJECT_POOLING_GLOSS"></span>**COM+ Object Pooling**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-172">Um serviço automático fornecido pelo COM+ que permite configurar um componente para que as instâncias dele sejam mantidas ativas em um pool, prontas para serem usadas por qualquer cliente que solicite o componente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-172">An automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**Partições COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-173"><span id="cos.complus_partitions_gloss"></span><span id="COS.COMPLUS_PARTITIONS_GLOSS"></span>**COM+ Partitions**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-174">Um serviço COM+ que habilita o, em um único computador, a criação de espaços de execução separados para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-174">A COM+ service that enables, on a single computer, the creation of separate execution spaces for applications.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**Conjuntos de partições COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-175"><span id="cos.complus_partition_sets_gloss"></span><span id="COS.COMPLUS_PARTITION_SETS_GLOSS"></span>**COM+ partition sets**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-176">Um grupo de partições COM+ que é mapeado para uma determinada ID de usuário no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-176">A group of COM+ partitions that is mapped to a particular user ID in Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**Componentes em fila COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-177"><span id="cos.complus_queued_components_gloss"></span><span id="COS.COMPLUS_QUEUED_COMPONENTS_GLOSS"></span>**COM+ Queued Components**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-178">Um serviço COM+, baseado no enfileiramento de mensagens da Microsoft, que fornece uma maneira fácil de invocar e executar componentes de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-178">A COM+ service, based on Microsoft Message Queuing, that provides an easy way to invoke and execute components asynchronously.</span></span> <span data-ttu-id="3aa2c-179">O processamento de mensagens pode ocorrer sem considerar a disponibilidade ou a acessibilidade do remetente ou do receptor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-179">Message processing can occur without regard to the availability or accessibility of either the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**Aplicativo de servidor COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-180"><span id="cos.complus_server_application_gloss"></span><span id="COS.COMPLUS_SERVER_APPLICATION_GLOSS"></span>**COM+ server application**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-181">Um aplicativo COM+ que é executado em seu próprio processo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-181">A COM+ application that runs in its own process.</span></span> <span data-ttu-id="3aa2c-182">Os aplicativos de servidor podem dar suporte a todos os serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-182">Server applications can support all COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**SOAP COM+**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-183"><span id="cos.complus_soap_gloss"></span><span id="COS.COMPLUS_SOAP_GLOSS"></span>**COM+ SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-184">Um recurso dos serviços de componentes que permite expor um aplicativo COM+ como um serviço Web XML.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-184">A Component Services feature that allows you to expose a COM+ application as an XML web service.</span></span> <span data-ttu-id="3aa2c-185">O SOAP COM+ também permite que você use um serviço Web XML como um componente COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-185">COM+ SOAP also enables you to use an XML web service as a COM component.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**Componente COM**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-186"><span id="cos.com_component_gloss"></span><span id="COS.COM_COMPONENT_GLOSS"></span>**COM component**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-187">Uma unidade binária de código que inclui o código de empacotamento e de registro e que cria objetos COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-187">A binary unit of code that includes packaging and registration code and that creates COM objects.</span></span> <span data-ttu-id="3aa2c-188">Todos os aplicativos COM+ consistem em um ou mais componentes COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-188">All COM+ applications consist of one or more COM components.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**confirmar árvore**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-189"><span id="cos.commit_tree_gloss"></span><span id="COS.COMMIT_TREE_GLOSS"></span>**commit tree**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-190">Em um sistema de transações distribuídas, a representação conceitual de uma transação é baseada nas relações hierárquicas entre os gerenciadores de transações individuais que participam de uma transação distribuída.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-190">In a distributed transaction system, the conceptual representation of a transaction as based on the hierarchical relationships between individual transaction managers participating in a distributed transaction.</span></span> <span data-ttu-id="3aa2c-191">Incluídos nessa hierarquia estão os gerenciadores de recursos inscritos associados aos gerenciadores de transações.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-191">Included in that hierarchy are the enlisted resource managers associated with the transaction managers.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**Objeto COM**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-192"><span id="cos.com_object_gloss"></span><span id="COS.COM_OBJECT_GLOSS"></span>**COM object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-193">No modelo de programação COM, uma estrutura de programação que encapsula os dados e a funcionalidade, que são definidos e alocados como uma única unidade e para o qual o único acesso público é através das interfaces da estrutura de programação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-193">In the COM programming model, a programming structure encapsulating both data and functionality, which are defined and allocated as a single unit and for which the only public access is through the programming structure's interfaces.</span></span> <span data-ttu-id="3aa2c-194">Um objeto COM deve dar suporte a, no mínimo, a interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , que mantém a existência do objeto enquanto ele está sendo usado e fornece acesso às outras interfaces do objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-194">A COM object must support, at a minimum, the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface, which maintains the object's existence while it is being used and provides access to the object's other interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos de compensação (CRM)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-195"><span id="cos.compensating_resource_manager_gloss"></span><span id="COS.COMPENSATING_RESOURCE_MANAGER_GLOSS"></span>**Compensating Resource Manager (CRM)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-196">Um recurso COM+ que permite que recursos não transacionais participem de uma transação de confirmação de duas fases com o Microsoft Coordenador de Transações Distribuídas (DTC).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-196">A COM+ feature that enables non-transactional resources to participate in a two-phase commit transaction with the Microsoft Distributed Transaction Coordinator (DTC).</span></span> <span data-ttu-id="3aa2c-197">Normalmente, o CRMs não fornece os recursos de isolamento de gerenciadores de recursos completos, mas eles fornecem atomicidade transacional e durabilidade ao gravar em um log.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-197">Typically, CRMs do not provide the isolation capabilities of full resource managers, but they do provide transactional atomicity and durability by writing to a log.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-198"><span id="cos.component_services_administrative_tool_gloss"></span><span id="COS.COMPONENT_SERVICES_ADMINISTRATIVE_TOOL_GLOSS"></span>**Component Services administrative tool**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-199">Um snap-in de interface do usuário por meio do qual administradores e desenvolvedores podem criar, configurar e manter aplicativos COM+, bem como administrar transações distribuídas e bancos de dados residentes na memória.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-199">A user-interface snap-in through which administrators and developers can create, configure, and maintain COM+ applications, as well as administer distributed transactions and memory-resident databases.</span></span> <span data-ttu-id="3aa2c-200">A ferramenta administrativa serviços de componentes também pode ser usada para exibir eventos do sistema e gerenciar serviços do sistema locais no computador em que a ferramenta está instalada.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-200">The Component Services administrative tool can also be used to view system events and manage system services local to the computer on which the tool is installed.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**modelo conceitual**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-201"><span id="cos.conceptual_model_gloss"></span><span id="COS.CONCEPTUAL_MODEL_GLOSS"></span>**conceptual model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-202">A primeira etapa na fase de design do aplicativo COM+, em que o desenvolvedor define os problemas de negócios a serem resolvidos e decide quais componentes e serviços são necessários.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-202">The first step in the COM+ application design phase, where the developer defines the business problems to be solved and decides what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**corrente**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-203"><span id="cos.concurrency_gloss"></span><span id="COS.CONCURRENCY_GLOSS"></span>**concurrency**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-204">A capacidade de mais de uma transação ou processo de acessar os mesmos dados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-204">The ability of more than one transaction or process to access the same data at the same time.</span></span> <span data-ttu-id="3aa2c-205">O COM+ geralmente gerencia a simultaneidade por meio da sincronização.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-205">COM+ generally manages concurrency through synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**componente configurado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-206"><span id="cos.configured_component_gloss"></span><span id="COS.CONFIGURED_COMPONENT_GLOSS"></span>**configured component**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-207">Um componente COM que foi instalado em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-207">A COM component that has been installed into a COM+ application.</span></span> <span data-ttu-id="3aa2c-208">Depois de instalado, o componente é configurado no catálogo COM+ para usar os serviços COM+ disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-208">After it is installed, the component is configured within the COM+ catalog to make use of the available COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**noticioso**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-209"><span id="cos.context_gloss"></span><span id="COS.CONTEXT_GLOSS"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-210">Um conjunto de propriedades de tempo de execução associadas a um ou mais objetos COM que são usados para fornecer serviços para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-210">A set of run-time properties associated with one or more COM objects that are used to provide services for those objects.</span></span> <span data-ttu-id="3aa2c-211">Cada objeto COM é executado em um único contexto de ativação para desativação (sempre dentro do mesmo apartamento).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-211">Every COM object runs in a single context from activation to deactivation (always within the same apartment).</span></span> <span data-ttu-id="3aa2c-212">Inicializado quando um objeto é ativado, as propriedades de contexto, como propriedades de contexto de segurança, representam as necessidades de tempo de execução de um objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-212">Initialized when an object is activated, context properties, such as security context properties, represent the run-time needs of an object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**camada de dados**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-213"><span id="cos.data_tier_gloss"></span><span id="COS.DATA_TIER_GLOSS"></span>**data tier**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-214">No modelo de arquitetura de três camadas para aplicativos de negócios, a camada de acesso do DBMS, que pode ser acessada por meio da camada intermediária, ou do serviço de negócios, e às vezes por meio da camada de apresentação ou de serviços do usuário.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-214">In the three-tier architecture model for business applications, the DBMS access layer, which can be accessed through the middle tier, or business services layer, and on occasion through the presentation tier, or user services layer.</span></span> <span data-ttu-id="3aa2c-215">A camada de dados consiste em componentes de acesso a dados (em vez de conexões brutas de DBMS) para auxiliar no compartilhamento de recursos e permitir que os clientes sejam configurados sem instalar as bibliotecas DBMS e os drivers ODBC em cada cliente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-215">The data tier consists of data access components (rather than raw DBMS connections) to aid in resource sharing and to allow clients to be configured without installing the DBMS libraries and ODBC drivers on each client.</span></span> <span data-ttu-id="3aa2c-216">Também chamada de *camada de serviços de dados*.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-216">Also called *data services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**bloqueado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-217"><span id="cos.deadlock_gloss"></span><span id="COS.DEADLOCK_GLOSS"></span>**deadlock**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-218">Em aplicativos multissegmentados, um problema de Threading que ocorre quando cada membro de um conjunto de threads está aguardando outro membro do conjunto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-218">In multithreaded applications, a threading problem that occurs when each member of a set of threads is waiting for another member of the set.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**Delegação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-219"><span id="cos.delegation_gloss"></span><span id="COS.DELEGATION_GLOSS"></span>**delegation**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-220">Uma forma de representação que autoriza um servidor a agir em nome de um cliente, dando ao servidor a capacidade de representar clientes pela rede.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-220">A form of impersonation that authorizes a server to act on a client's behalf, giving the server the ability to impersonate clients over the network.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**transação distribuída**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-221"><span id="cos.distributed_transaction_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_GLOSS"></span>**distributed transaction**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-222">Uma transação que envolve vários gerenciadores de recursos, que podem estar no mesmo computador ou em computadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-222">A transaction that involves multiple resource managers, which can be on the same or different computers.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Coordenador de Transações Distribuídas (DTC)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-223"><span id="cos.distributed_transaction_coordinator_gloss"></span><span id="COS.DISTRIBUTED_TRANSACTION_COORDINATOR_GLOSS"></span>**Distributed Transaction Coordinator (DTC)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-224">Um serviço do sistema que gerencia transações e comunicações relacionadas à transação que são distribuídas por dois ou mais gerenciadores de recursos em um ou mais sistemas para garantir as transações ACID corretas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-224">A system service that manages transactions and transaction-related communications that are distributed across two or more resource managers on one or more systems to ensure correct ACID transactions.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**encobrimento dinâmico**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-225"><span id="cos.dynamic_cloaking_gloss"></span><span id="COS.DYNAMIC_CLOAKING_GLOSS"></span>**dynamic cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-226">Uma forma de encobrir onde a identidade do cliente original é descoberta como o token de acesso de thread do servidor em cada chamada de método para o servidor downstream.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-226">A form of cloaking where the original client identity is discovered as the server thread access token on each method call to the downstream server.</span></span> <span data-ttu-id="3aa2c-227">Embora a identidade apresentada possa ser determinada dinamicamente, a sobrecarga necessária para fazer isso pode ser consideravelmente mais cara.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-227">Although the identity that is presented can be determined dynamically, the overhead required to do this can be considerably more expensive.</span></span> <span data-ttu-id="3aa2c-228">Para aplicativos COM+, a configuração padrão é para o recurso de encobrimento dinâmico porque fornece a flexibilidade que geralmente é exigida pelas circunstâncias que precisam usar a representação em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-228">For COM+ applications, the default configuration is for dynamic cloaking capability because it provides the flexibility that is usually required by circumstances that necessitate using impersonation in the first place.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**objeto Enumerator**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-229"><span id="cos.enumerator_object_gloss"></span><span id="COS.ENUMERATOR_OBJECT_GLOSS"></span>**enumerator object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-230">Habilita a enumeração de itens nas coleções.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-230">Enables enumeration of items in a collection.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**circunstância**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-231"><span id="cos.event_gloss"></span><span id="COS.EVENT_GLOSS"></span>**event**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-232">Uma ação reconhecida por um objeto, como clicar no mouse ou pressionar uma tecla, e para a qual você pode escrever código para responder.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-232">An action recognized by an object, such as clicking the mouse or pressing a key, and for which you can write code to respond.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**objeto de classe de evento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-233"><span id="cos.event_class_object_gloss"></span><span id="COS.EVENT_CLASS_OBJECT_GLOSS"></span>**event class object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-234">Um componente configurado que fornece um registro persistente no sistema de eventos COM+ para descrever os Publicadores e as interfaces de acionamento associadas a esses Publicadores.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-234">A configured component that provides a persistent record in the COM+ event system to describe the publishers and the firing interfaces associated with those publishers.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**método de evento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-235"><span id="cos.event_method_gloss"></span><span id="COS.EVENT_METHOD_GLOSS"></span>**event method**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-236">Um método em uma interface COM+ que identifica um evento COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-236">A method in a COM+ interface that identifies a COM+ event.</span></span> <span data-ttu-id="3aa2c-237">Os métodos de evento devem ser nomeados exclusivamente e podem conter apenas parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-237">Event methods must be uniquely named and can contain only input parameters.</span></span> <span data-ttu-id="3aa2c-238">O valor de retorno deve ser um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-238">The return value must be an **HRESULT**.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**objeto de evento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-239"><span id="cos.event_object_gloss"></span><span id="COS.EVENT_OBJECT_GLOSS"></span>**event object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-240">Um objeto COM que pode sinalizar um ou mais threads que um evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-240">A COM object that can signal one or more threads that an event has occurred.</span></span> <span data-ttu-id="3aa2c-241">Qualquer thread dentro de um processo pode criar um objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-241">Any thread within a process can create an event object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**Exception**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-242"><span id="cos.exception_gloss"></span><span id="COS.EXCEPTION_GLOSS"></span>**exception**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-243">Uma condição anormal ou um erro que ocorre durante a execução de um programa e que requer a execução de software fora do fluxo de controle normal.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-243">An abnormal condition or error that occurs during the execution of a program and that requires the execution of software outside the normal flow of control.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**pós-falha**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-244"><span id="cos.failover_gloss"></span><span id="COS.FAILOVER_GLOSS"></span>**failover**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-245">Em um sistema de rede de cluster, o processo de realocar um recurso sobrecarregado ou com falha, como um servidor, uma unidade de disco ou uma rede, para seu componente de backup.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-245">In a cluster network system, the process of relocating an overloaded or failed resource—such as a server, a disk drive, or a network—to its backup component.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**processo de thread livre**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-246"><span id="cos.free_threaded_process_gloss"></span><span id="COS.FREE_THREADED_PROCESS_GLOSS"></span>**free-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-247">Um processo que tem um apartamento multithread e nenhum Apartments de thread único.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-247">A process that has a multithreaded apartment and no single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**Coordenador de confirmação global**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-248"><span id="cos.global_commit_coordinator_gloss"></span><span id="COS.GLOBAL_COMMIT_COORDINATOR_GLOSS"></span>**global commit coordinator**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-249">Em um sistema de transações distribuídas baseado no Microsoft Windows, o Gerenciador de transações raiz da árvore de confirmação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-249">On a Microsoft Windows–based distributed transaction system, the root transaction manager of the commit tree.</span></span> <span data-ttu-id="3aa2c-250">Esse coordenador toma a decisão de confirmar ou anular uma determinada transação e nunca é duvidoso.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-250">This coordinator makes the decision to either commit or abort a given transaction and is never in doubt.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**representação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-251"><span id="cos.impersonation_gloss"></span><span id="COS.IMPERSONATION_GLOSS"></span>**impersonation**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-252">A capacidade de execução de um thread em um contexto de segurança diferente daquele do processo que possui o thread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-252">The ability of a thread to execute in a security context different from that of the process owning the thread.</span></span> <span data-ttu-id="3aa2c-253">O thread do servidor usa um token de acesso que representa as credenciais do cliente e, com isso, ele pode acessar recursos que o cliente pode acessar.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-253">The server thread uses an access token representing the client's credentials, and with this, it can access resources that the client can access.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**nível de representação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-254"><span id="cos.impersonation_level_gloss"></span><span id="COS.IMPERSONATION_LEVEL_GLOSS"></span>**impersonation level**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-255">A configuração usada pelo cliente para conceder ao servidor um nível específico de autoridade para executar ações em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-255">The setting used by the client to grant the server a particular level of authority to carry out actions on the client's behalf.</span></span> <span data-ttu-id="3aa2c-256">No COM+, isso pode ser definido somente para aplicativos de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-256">In COM+, this can be set only for COM+ server applications.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interceptação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-257"><span id="cos.interception_gloss"></span><span id="COS.INTERCEPTION_GLOSS"></span>**interception**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-258">Para um objeto ativado em um determinado contexto, o processo de tratamento de chamadas para esse objeto entre o limite de contexto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-258">For an object activated in a given context, the process of handling calls to that object from across the context boundary.</span></span> <span data-ttu-id="3aa2c-259">Chamadas no contexto são manipuladas com proxies de interface leves que manipularão qualquer mediação necessária para ajustar o ambiente de tempo de execução de um que acomoda o chamador para um que acomoda o receptor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-259">Calls across context are handled with lightweight interface proxies that will handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-260"><span id="cos.interface_gloss"></span><span id="COS.INTERFACE_GLOSS"></span>**interface**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-261">Na programação baseada em COM, uma coleção de funções públicas relacionadas que fornecem acesso a um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-261">In COM-based programming, a collection of related public functions that provide access to a COM object.</span></span> <span data-ttu-id="3aa2c-262">O conjunto de interfaces em um objeto COM compõe um contrato que especifica como programas e outros objetos podem interagir com o objeto COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-262">The set of interfaces on a COM object composes a contract that specifies how programs and other objects can interact with the COM object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**proxy de interface**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-263"><span id="cos.interface_proxy_gloss"></span><span id="COS.INTERFACE_PROXY_GLOSS"></span>**interface proxy**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-264">Um objeto específico de interface que empacota (empacota) parâmetros para essa interface em preparação para uma chamada de método remota e desempacota (unmarshals) os valores de retorno do stub da interface.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-264">An interface-specific object that packages (marshals) parameters for that interface in preparation for a remote method call and unpackages (unmarshals) the return values from the interface stub.</span></span> <span data-ttu-id="3aa2c-265">Um proxy é executado no espaço de endereço do remetente e se comunica com um stub correspondente no espaço de endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-265">A proxy runs in the address space of the sender and communicates with a corresponding stub in the receiver's address space.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**stub da interface**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-266"><span id="cos.interface_stub_gloss"></span><span id="COS.INTERFACE_STUB_GLOSS"></span>**interface stub**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-267">Um objeto específico da interface que desempacota parâmetros empacotados, chama o método necessário e pacotes (Marshals) retorna valores do método chamado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-267">An interface-specific object that unpackages marshaled parameters, calls the required method, and packages (marshals) return values from the called method.</span></span> <span data-ttu-id="3aa2c-268">O stub é executado no espaço de endereço do destinatário e se comunica com um proxy de interface correspondente no espaço de endereço do remetente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-268">The stub runs in the receiver's address space and communicates with a corresponding interface proxy in the sender's address space.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**objeto interior**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-269"><span id="cos.interior_object_gloss"></span><span id="COS.INTERIOR_OBJECT_GLOSS"></span>**interior object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-270">Em uma hierarquia transacional, qualquer objeto sob o objeto raiz.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-270">In a transactional hierarchy, any object under the root object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**ativação JIT (just-in-time)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-271"><span id="cos.just_in_time_activation_gloss"></span><span id="COS.JUST_IN_TIME_ACTIVATION_GLOSS"></span>**just-in-time (JIT) activation**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-272">Um serviço automático fornecido pelo COM+ que permite que os recursos do servidor ocioso sejam usados de forma mais produtiva.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-272">An automatic service provided by COM+ that allows idle server resources to be used more productively.</span></span> <span data-ttu-id="3aa2c-273">Quando um componente é configurado como JIT ativado, o COM+ pode desativar uma instância dele enquanto um cliente ainda mantém uma referência ativa ao objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-273">When a component is configured as JIT activated, COM+ can deactivate an instance of it while a client still holds an active reference to the object.</span></span> <span data-ttu-id="3aa2c-274">Na próxima vez que o cliente chamar um método no objeto, o COM+ reativará o objeto de forma transparente para o cliente, just-in-time.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-274">The next time the client calls a method on the object, COM+ will reactivate the object transparently to the client, just in time.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**componente herdado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-275"><span id="cos.legacy_component_gloss"></span><span id="COS.LEGACY_COMPONENT_GLOSS"></span>**legacy component**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-276">Um componente não configurado que foi instalado em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-276">An unconfigured component that has been installed into a COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**Listener**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-277"><span id="cos.listener_gloss"></span><span id="COS.LISTENER_GLOSS"></span>**listener**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-278">Um elemento de arquitetura do serviço de componentes em fila do COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-278">An architectural element of the COM+ Queued Components service.</span></span> <span data-ttu-id="3aa2c-279">O ouvinte é um objeto COM que abre a fila de mensagens associada ao seu aplicativo host e aguarda que as mensagens cheguem.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-279">The listener is a COM object that opens the message queue associated with its host application and waits for messages to arrive.</span></span> <span data-ttu-id="3aa2c-280">À medida que as mensagens chegam, o ouvinte despacha threads que processam mensagens.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-280">As messages arrive, the listener dispatches threads that process messages.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**modelo lógico**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-281"><span id="cos.logical_model_gloss"></span><span id="COS.LOGICAL_MODEL_GLOSS"></span>**logical model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-282">A segunda etapa em um processo de design de aplicativo COM+, em que o modelo conceitual é dividido em camadas lógicas da arquitetura de três camadas, da seguinte maneira: a camada de apresentação ou os serviços de usuário; a camada intermediária ou os serviços corporativos; e a camada de dados ou serviços de dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-282">The second step in a COM+ application design process, where the conceptual model is broken out into the logical tiers of the three-tier architecture, as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**evento livremente acoplado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-283"><span id="cos.loosely_couple_event_gloss"></span><span id="COS.LOOSELY_COUPLE_EVENT_GLOSS"></span>**loosely coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-284">Um evento cujo remetente (Publicador) e destinatário (assinante) não estão ligados de forma rigorosa.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-284">An event whose sender (publisher) and receiver (subscriber) are not closely bound.</span></span> <span data-ttu-id="3aa2c-285">Em um sistema de eventos menos rígido, como eventos COM+, as informações de eventos de editores diferentes são mantidas em um repositório de eventos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-285">In a loosely coupled event system, such as COM+ Events, event information from different publishers is persisted in an event store.</span></span> <span data-ttu-id="3aa2c-286">Os assinantes consultam esse armazenamento e selecionam os eventos que desejam receber.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-286">Subscribers query this store and select the events that they want to receive.</span></span> <span data-ttu-id="3aa2c-287">A seleção de informações de evento no repositório de eventos cria uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-287">Selecting event information from the event store creates a subscription.</span></span> <span data-ttu-id="3aa2c-288">Quando ocorre um evento, o sistema de eventos examina esse banco de dados e encontra os assinantes interessados, cria um novo objeto de cada classe interessada e chama um método nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-288">When an event occurs, the event system looks in this database and finds the interested subscribers, creates a new object of each interested class, and calls a method on that object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-289"><span id="cos.marshaling_gloss"></span><span id="COS.MARSHALING_GLOSS"></span>**marshaling**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-290">O processo de empacotamento e desempacotamento de parâmetros do método de interface entre limites de thread ou processo para que uma chamada de procedimento remota possa ocorrer.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-290">The process of packaging and unpackaging interface method parameters across thread or process boundaries so that a remote procedure call can take place.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**movimentador de mensagem**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-291"><span id="cos.message_mover_gloss"></span><span id="COS.MESSAGE_MOVER_GLOSS"></span>**message mover**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-292">O elemento arquitetônico do serviço de componentes em fila do COM+ que move mensagens com falha de volta para sua fila de entrada para que elas possam ser repetidas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-292">The architectural element of the COM+ Queued Components service that moves failed messages back to their input queue so that they can be retried.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-evento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-293"><span id="cos.meta_event_gloss"></span><span id="COS.META_EVENT_GLOSS"></span>**meta-event**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-294">Um tipo de evento usado pelo sistema de eventos COM+ para notificar os assinantes interessados sempre que os objetos ou assinaturas da classe de evento forem criados, modificados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-294">A type of event used by the COM+ Events system to notify interested subscribers whenever event class objects or subscriptions are created, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**forma**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-295"><span id="cos.method_gloss"></span><span id="COS.METHOD_GLOSS"></span>**method**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-296">Na programação baseada em COM, um processo executado por um objeto COM quando recebe uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-296">In COM-based programming, a process performed by a COM object when it receives a message.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**camada intermediária**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-297"><span id="cos.middle_tier_gloss"></span><span id="COS.MIDDLE_TIER_GLOSS"></span>**middle tier**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-298">No modelo de arquitetura de três camadas para aplicativos de negócios, a camada que consiste na lógica de negócios e nas regras de dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-298">In the three-tier architecture model for business applications, the layer comprising the business logic and data rules.</span></span> <span data-ttu-id="3aa2c-299">Os componentes que compõem a camada intermediária podem ser usados para impor regras de negócio, como algoritmos de negócios, regulamentos legais ou governamentais, e regras de dados, que são projetadas para manter as estruturas de dados consistentes em um ou vários bancos de dado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-299">The components that make up the middle tier can be used to enforce business rules, such as business algorithms, legal or governmental regulations, and data rules, which are designed to keep the data structures consistent within either specific or multiple databases.</span></span> <span data-ttu-id="3aa2c-300">Como esses componentes de camada intermediária não estão vinculados a um cliente específico, eles podem ser usados por todos os aplicativos e podem ser movidos para locais diferentes conforme o tempo de resposta e outras regras exigem.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-300">Because these middle-tier components are not tied to a specific client, they can be used by all applications and can be moved to different locations as response time and other rules require.</span></span> <span data-ttu-id="3aa2c-301">Também chamada de *camada de serviços comerciais* ou camada de *lógica de negócios*.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-301">Also called *business services layer* or *business logic tier*.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**processo de modelo misto**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-302"><span id="cos.mixed_model_process_gloss"></span><span id="COS.MIXED_MODEL_PROCESS_GLOSS"></span>**mixed model process**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-303">Um processo que tem um apartamento multithread e um ou mais Apartments de thread único.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-303">A process that has a multithreaded apartment and one or more single-threaded apartments.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-304"><span id="cos.moniker_gloss"></span><span id="COS.MONIKER_GLOSS"></span>**moniker**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-305">Um nome que identifica exclusivamente um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-305">A name that uniquely identifies a COM object.</span></span> <span data-ttu-id="3aa2c-306">Da mesma forma que um caminho identifica um arquivo no sistema de arquivos, um moniker identifica um objeto COM no namespace do diretório.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-306">In the same way that a path identifies a file in the file system, a moniker identifies a COM object in the directory namespace.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**arquivo. msi**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-307"><span id="cos.msi_file_gloss"></span><span id="COS.MSI_FILE_GLOSS"></span>**.msi file**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-308">Um arquivo criado pela ferramenta administrativa serviços de componentes quando você exporta um aplicativo COM+ ou proxy de aplicativo para instalação em outro computador.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-308">A file created by the Component Services administrative tool when you export a COM+ application or application proxy for installation on another computer.</span></span> <span data-ttu-id="3aa2c-309">O arquivo. msi pode ser instalado em qualquer cliente baseado no Windows usando Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-309">The .msi file can be installed on any Windows-based client using Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento multithread**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-310"><span id="cos.multithreaded_apartment_model_gloss"></span><span id="COS.MULTITHREADED_APARTMENT_MODEL_GLOSS"></span>**multithreaded apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-311">Um modelo de apartamento no qual todos os threads no processo que foram inicializados como de thread livre residem em um único apartamento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-311">An apartment model in which all the threads in the process that have been initialized as free-threaded reside in a single apartment.</span></span> <span data-ttu-id="3aa2c-312">Portanto, não há necessidade de realizar marshaling entre threads.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-312">Therefore, there is no need to marshal between threads.</span></span> <span data-ttu-id="3aa2c-313">Os threads não precisam recuperar e despachar mensagens porque o COM não usa mensagens de janela neste modelo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-313">The threads need not retrieve and dispatch messages because COM does not use window messages in this model.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**transação aninhada**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-314"><span id="cos.nested_transaction_gloss"></span><span id="COS.NESTED_TRANSACTION_GLOSS"></span>**nested transaction**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-315">Uma transação secundária iniciada de dentro de um limite de transação primária ou pai existente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-315">A secondary transaction initiated from within an existing primary or parent transaction boundary.</span></span> <span data-ttu-id="3aa2c-316">A transação primária não é confirmada até que todas as suas transações subordinadas ou aninhadas sejam confirmadas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-316">The primary transaction does not commit until all of its subordinate, or nested, transactions commit.</span></span> <span data-ttu-id="3aa2c-317">COM+ não dá suporte a transações aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-317">COM+ does not support nested transactions.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**modelo de apartamento neutro**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-318"><span id="cos.neutral_apartment_model_gloss"></span><span id="COS.NEUTRAL_APARTMENT_MODEL_GLOSS"></span>**neutral apartment model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-319">Um modelo de threading no qual os objetos seguem as diretrizes para Apartments multithread, mas podem ser executados em qualquer tipo de thread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-319">A threading model in which objects follow the guidelines for multithreaded apartments but can execute on any kind of thread.</span></span> <span data-ttu-id="3aa2c-320">O modelo de apartamento neutro é o modelo de Threading recomendado para componentes COM e aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-320">The neutral apartment model is the recommended threading model for COM components and COM+ applications.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**objeto persistente**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-321"><span id="cos.persistent_object_gloss"></span><span id="COS.PERSISTENT_OBJECT_GLOSS"></span>**persistent object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-322">Um objeto COM que pode salvar seu estado interno quando solicitado por um cliente e que esteja em conformidade com os padrões definidos pelo COM por meio dos quais os clientes podem solicitar que os objetos sejam inicializados, carregados e salvos em e de um repositório de dados (por exemplo, arquivo simples, armazenamento estruturado ou memória).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-322">A COM object that can save its internal state when asked to do so by a client and that conforms to COM-defined standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="3aa2c-323">É responsabilidade do cliente gerenciar o local onde os dados persistentes do objeto são armazenados, mas não o formato dos dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-323">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**interface de objeto persistente**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-324"><span id="cos.persistent_object_interface_gloss"></span><span id="COS.PERSISTENT_OBJECT_INTERFACE_GLOSS"></span>**persistent object interface**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-325">Uma interface COM implementada por um objeto persistente.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-325">A COM interface implemented by a persistent object.</span></span> <span data-ttu-id="3aa2c-326">Os clientes usam interfaces de objeto persistentes para informar a esses objetos persistentes quando e onde armazenar seu estado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-326">Clients use persistent object interfaces to tell those persistent objects when and where to store their state.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**interface de notificação de fase zero**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-327"><span id="cos.phase_zero_notification_interface_gloss"></span><span id="COS.PHASE_ZERO_NOTIFICATION_INTERFACE_GLOSS"></span>**phase zero notification interface**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-328">Interface COM+ que permite que os aplicativos detectem quando uma transação está pronta para prosseguir com um protocolo de confirmação de duas fases para que possa executar as operações de notificação necessárias e se comunicar com o Gerenciador de transações quando as operações forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-328">COM+ interface that allows applications to detect when a transaction is ready to proceed with a two-phase commit protocol so that it can perform the necessary notification operations and communicate to the transaction manager when the operations have been completed.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**modelo físico**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-329"><span id="cos.physical_model_gloss"></span><span id="COS.PHYSICAL_MODEL_GLOSS"></span>**physical model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-330">A terceira e última etapa no processo de design do aplicativo COM+, em que o desenvolvedor determina onde os componentes residem fisicamente e como eles devem ser codificados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-330">The third and final step in the COM+ application design process, where the developer determines where the components reside physically and how they are to be coded.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**Player**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-331"><span id="cos.player_gloss"></span><span id="COS.PLAYER_GLOSS"></span>**player**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-332">O elemento de arquitetura do serviço de componentes em fila do COM+ que recupera a mensagem de uma fila e, em seguida, carrega o objeto de servidor e os stubs de interface padrão para desempacotar dados e invocar métodos de servidor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-332">The architectural element of the COM+ Queued Components service that retrieves the message from a queue and then loads the server object and the standard interface stubs to unmarshal data and invoke server methods.</span></span> <span data-ttu-id="3aa2c-333">O Player desempacota o contexto de segurança do cliente no lado do servidor e, em seguida, invoca o componente do servidor e faz as mesmas chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-333">The player unmarshals the client's security context at the server side and then invokes the server component and makes the same method calls.</span></span> <span data-ttu-id="3aa2c-334">As chamadas de método não são reproduzidas pelo Player até que o componente cliente seja concluído e a transação que registrou o método chame confirmações.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-334">The method calls are not played back by the player until the client component completes and the transaction that recorded the method calls commits.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**camada de apresentação**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-335"><span id="cos.presentation_tier_gloss"></span><span id="COS.PRESENTATION_TIER_GLOSS"></span>**presentation tier**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-336">No modelo de arquitetura de três camadas para aplicativos de negócios, a camada que apresenta os dados para o usuário e, opcionalmente, permite a manipulação de dados e a entrada de dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-336">In the three-tier architecture model for business applications, the layer that presents data to the user and optionally permits data manipulation and data entry.</span></span> <span data-ttu-id="3aa2c-337">Os dois tipos principais de interface do usuário para a camada de apresentação são o aplicativo tradicional e o aplicativo baseado na Web.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-337">The two main types of user interface for the presentation tier are the traditional application and the Web-based application.</span></span> <span data-ttu-id="3aa2c-338">Também chamada de *camada de serviços de usuário*.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-338">Also called *user services layer*.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**token de acesso primário**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-339"><span id="cos.primary_access_token_gloss"></span><span id="COS.PRIMARY_ACCESS_TOKEN_GLOSS"></span>**primary access token**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-340">Descreve o contexto de segurança da conta de usuário associada a um processo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-340">Describes the security context of the user account associated with a process.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**Gerenciador de proxy**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-341"><span id="cos.proxy_manager_gloss"></span><span id="COS.PROXY_MANAGER_GLOSS"></span>**proxy manager**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-342">No empacotamento padrão, um componente que gerencia todos os proxies de interface para um único objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-342">In standard marshaling, a component that manages all the interface proxies for a single object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo objeto**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-343"><span id="cos.pseudo_object_gloss"></span><span id="COS.PSEUDO_OBJECT_GLOSS"></span>**pseudo-object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-344">Um tipo de objeto contido, como uma seleção de usuário em um documento, um intervalo de células em uma planilha ou um intervalo de caracteres em um documento de texto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-344">A type of contained object, such as a user selection in a document, a range of cells in a spreadsheet, or a range of characters in a text document.</span></span> <span data-ttu-id="3aa2c-345">Esse tipo de objeto é chamado de pseudo-objeto porque não é tratado como um objeto distinto até que um usuário marque a seleção.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-345">This type of object is called a pseudo-object because it isn't treated as a distinct object until a user marks the selection.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**programa**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-346"><span id="cos.publisher_gloss"></span><span id="COS.PUBLISHER_GLOSS"></span>**publisher**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-347">O remetente de um evento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-347">The sender of an event.</span></span> <span data-ttu-id="3aa2c-348">Na arquitetura de eventos COM+, o Publicador faz a chamada de método para iniciar um evento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-348">In the COM+ Events architecture, the publisher makes the method call to initiate an event.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**moniker da fila**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-349"><span id="cos.queue_moniker_gloss"></span><span id="COS.QUEUE_MONIKER_GLOSS"></span>**queue moniker**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-350">O moniker usado para ativar um componente enfileirado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-350">The moniker used to activate a queued component.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**condição de corrida**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-351"><span id="cos.race_condition_gloss"></span><span id="COS.RACE_CONDITION_GLOSS"></span>**race condition**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-352">Em um aplicativo multithread, uma condição que ocorre quando vários threads acessam um item de dados sem coordenação, possivelmente causando resultados inconsistentes, dependendo de qual thread atinge o item de dados primeiro.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-352">In a multithreaded application, a condition that occurs when multiple threads access a data item without coordination, possibly causing inconsistent results, depending on which thread reaches the data item first.</span></span> <span data-ttu-id="3aa2c-353">O COM fornece algumas funções projetadas especificamente para ajudar a evitar condições de corrida em servidores fora do processo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-353">COM supplies some functions specifically designed to help avoid race conditions in out-of-process servers.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**gravador**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-354"><span id="cos.recorder_gloss"></span><span id="COS.RECORDER_GLOSS"></span>**recorder**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-355">O elemento arquitetônico do serviço de componentes em fila do COM+ que realiza marshaling do contexto de segurança do cliente em uma mensagem e registra todas as chamadas de método para um objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-355">The architectural element of the COM+ Queued Components service that marshals the client's security context into a message and records all of the method calls for an object.</span></span> <span data-ttu-id="3aa2c-356">O gravador é um Gerenciador de proxy fornecido pelo sistema que seleciona interfaces das interfaces queuable no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-356">The recorder is a system-provided proxy manager that selects interfaces from the queuable interfaces in the COM+ catalog.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**dispensador de recursos**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-357"><span id="cos.resource_dispenser_gloss"></span><span id="COS.RESOURCE_DISPENSER_GLOSS"></span>**resource dispenser**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-358">No modelo de programação COM+, um componente que gerencia o estado compartilhado não durável em nome dos componentes do aplicativo dentro de um processo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-358">In the COM+ programming model, a component that manages nondurable shared state on behalf of the application components within a process.</span></span> <span data-ttu-id="3aa2c-359">Os dispensadores de recursos são semelhantes aos gerenciadores de recursos, mas sem a garantia de durabilidade.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-359">Resource dispensers are similar to resource managers but without the guarantee of durability.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**Gerenciador de recursos**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-360"><span id="cos.resource_manager_gloss"></span><span id="COS.RESOURCE_MANAGER_GLOSS"></span>**resource manager**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-361">Um serviço que gerencia dados persistentes ou duráveis em bancos de dado, filas de mensagens duráveis ou sistemas de arquivos transacionais.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-361">A service that manages persistent or durable data in databases, durable message queues, or transactional file systems.</span></span> <span data-ttu-id="3aa2c-362">É o Gerenciador de recursos que sabe como armazenar dados e executar a recuperação de desastres.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-362">It is the resource manager that knows how to store data and perform disaster recovery.</span></span> <span data-ttu-id="3aa2c-363">Os aplicativos de servidor COM+ usam os gerenciadores de recursos para manter o estado durável de um aplicativo, como o registro de estoque disponível, pedidos pendentes e contas a receber.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-363">COM+ server applications use resource managers to maintain the durable state of an application, such as the record of inventory on hand, pending orders, and accounts receivable.</span></span> <span data-ttu-id="3aa2c-364">Os gerenciadores de recursos trabalham em cooperação com o Microsoft Coordenador de Transações Distribuídas (DTC) para garantir a atomicidade e o isolamento de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-364">Resource managers work in cooperation with the Microsoft Distributed Transaction Coordinator (DTC) to guarantee atomicity and isolation to an application.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**segurança baseada em função**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-365"><span id="cos.role_baed_security_gloss"></span><span id="COS.ROLE_BAED_SECURITY_GLOSS"></span>**role-based security**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-366">Um serviço de segurança COM+ fornecido para aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-366">A COM+ security service provided for COM+ applications.</span></span> <span data-ttu-id="3aa2c-367">Uma função representa uma categoria de usuários definida para um aplicativo COM+ com a finalidade de determinar as permissões de acesso aos recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-367">A role represents a category of users defined for a COM+ application for the purpose of determining access permissions to the application's resources.</span></span> <span data-ttu-id="3aa2c-368">As funções são atribuídas por um desenvolvedor a componentes, interfaces e métodos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-368">Roles are assigned by a developer to components, interfaces, and methods.</span></span> <span data-ttu-id="3aa2c-369">Os usuários são atribuídos por um administrador às funções apropriadas, permitindo que um usuário em uma determinada função acesse todos os recursos aos quais essa função está atribuída.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-369">Users are assigned by an administrator to appropriate roles, enabling a user within a given role to access any resources to which that role is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**objeto raiz**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-370"><span id="cos.root_object_gloss"></span><span id="COS.ROOT_OBJECT_GLOSS"></span>**root object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-371">O primeiro objeto de uma transação, chamado de raiz da transação e sempre colocado em um novo limite transacional.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-371">The first object of a transaction, called the root of the transaction, and always placed in a new transactional boundary.</span></span> <span data-ttu-id="3aa2c-372">Pode haver apenas um objeto raiz em uma transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-372">There can be only one root object in a transaction.</span></span> <span data-ttu-id="3aa2c-373">Todos os outros objetos na hierarquia transacional sob o objeto raiz são chamados de objetos interiores.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-373">All other objects in the transactional hierarchy under the root object are called interior objects.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**Gerenciador de transações raiz**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-374"><span id="cos.root_transaction_manager_gloss"></span><span id="COS.ROOT_TRANSACTION_MANAGER_GLOSS"></span>**root transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-375">O Gerenciador de transações no sistema que inicia uma transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-375">The transaction manager on the system that initiates a transaction.</span></span> <span data-ttu-id="3aa2c-376">A transação não é finalizada até que o Gerenciador de transações raiz determine o status da transação (confirmada ou anulada).</span><span class="sxs-lookup"><span data-stu-id="3aa2c-376">The transaction is not finalized until the root transaction manager determines the transaction's status (either committed or aborted).</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**sinal**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-377"><span id="cos.semaphore_gloss"></span><span id="COS.SEMAPHORE_GLOSS"></span>**semaphore**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-378">Um objeto de kernel usado para arbitrar o acesso a um recurso compartilhado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-378">A kernel object used to arbitrate access to a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**SCM (Gerenciador de controle de serviço)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-379"><span id="cos.service_control_manager_gloss"></span><span id="COS.SERVICE_CONTROL_MANAGER_GLOSS"></span>**service control manager (SCM)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-380">Um processo do Microsoft Windows Server que gerencia todos os serviços no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-380">A Microsoft Windows server process that manages all the services in the Windows registry.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**Gerenciador de propriedades compartilhadas (SPM)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-381"><span id="cos.shared_property_manager_gloss"></span><span id="COS.SHARED_PROPERTY_MANAGER_GLOSS"></span>**shared property manager (SPM)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-382">No com+, um dispensador de recursos que você pode usar para compartilhar o estado não persistente entre vários objetos dentro de um processo de servidor.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-382">In Com+, a resource dispenser that you can use to share nonpersistent state among multiple objects within a server process.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**processo de thread único**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-383"><span id="cos.single_threaded_process_gloss"></span><span id="COS.SINGLE_THREADED_PROCESS_GLOSS"></span>**single-threaded process**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-384">Um processo que consiste em apenas um apartamento de thread único, que por sua vez consiste em exatamente um thread.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-384">A process that consists of just one single-threaded apartment, which in turn consists of exactly one thread.</span></span> <span data-ttu-id="3aa2c-385">Todos os objetos COM que residem em um apartamento de thread único podem receber chamadas de método somente de um thread que pertence a esse apartamento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-385">All COM objects that live in a single-threaded apartment can receive method calls from only the one thread that belongs to that apartment.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-386"><span id="cos.soap_gloss"></span><span id="COS.SOAP_GLOSS"></span>**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-387">Um protocolo simples baseado em XML para a troca de informações estruturadas e de tipo na Web.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-387">A simple, XML-based protocol for exchanging structured and type information on the Web.</span></span> <span data-ttu-id="3aa2c-388">O protocolo não contém nenhuma semântica de aplicativo ou de transporte, o que o torna altamente modular e extensível.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-388">The protocol contains no application or transport semantics, which makes it highly modular and extensible.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**dividir registro**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-389"><span id="cos.split_registration_gloss"></span><span id="COS.SPLIT_REGISTRATION_GLOSS"></span>**split registration**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-390">Para componentes que já são componentes COM e são usados no ambiente de serviços COM+, a disposição de registro na qual o aspecto básico de COM do registro é armazenado no registro do Windows e novos serviços e atributos COM+ (por exemplo, componentes na fila) são armazenados no banco de dados de registro do COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-390">For components that are already existing COM components and are used in the COM+ services environment, the registration arrangement in which the basic COM aspect of the registration is stored in the Windows registry and new COM+ services and attributes (for example, Queued Components) are stored in the COM+ Registration Database.</span></span> <span data-ttu-id="3aa2c-391">Cada atributo de componente é armazenado no registro do Windows ou no banco de dados de registro do COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-391">Each component attribute is stored in either the Windows registry or the COM+ Registration Database.</span></span> <span data-ttu-id="3aa2c-392">Os novos componentes COM são registrados exclusivamente no banco de dados de registro do COM+, com alguma duplicação no registro do Windows para que as ferramentas existentes possam usá-los.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-392">New COM components are registered exclusively in the COM+ Registration Database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**dinâmico**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-393"><span id="cos.stateful_gloss"></span><span id="COS.STATEFUL_GLOSS"></span>**stateful**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-394">Ou pertencer a um sistema ou processo que monitora todos os detalhes do estado de uma atividade na qual ele participa.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-394">Of or pertaining to a system or process that monitors all details of the state of an activity in which it participates.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**sem**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-395"><span id="cos.stateless_gloss"></span><span id="COS.STATELESS_GLOSS"></span>**stateless**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-396">Ou pertencer a um sistema ou processo que participa da atividade sem monitorar todos os detalhes de seu estado.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-396">Of or pertaining to a system or process that participates in activity without monitoring all details of its state.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**encobrimento estático**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-397"><span id="cos.static_cloaking_gloss"></span><span id="COS.STATIC_CLOAKING_GLOSS"></span>**static cloaking**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-398">Uma forma de encobrir onde a identidade do cliente original pode ser apresentada uma vez a um servidor downstream, definindo a identidade do cliente original uma vez no proxy.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-398">A form of cloaking where the original client identity can be presented once to a downstream server, setting the original client identity once on the proxy.</span></span> <span data-ttu-id="3aa2c-399">Essa identidade do cliente é apresentada como um token de thread do servidor que será usado em chamadas de método subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-399">This client identity is presented as a server thread token that will be used on subsequent method calls.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**farão**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-400"><span id="cos.subscriber_gloss"></span><span id="COS.SUBSCRIBER_GLOSS"></span>**subscriber**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-401">O destinatário de um evento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-401">The receiver of an event.</span></span> <span data-ttu-id="3aa2c-402">Na arquitetura de eventos COM+, o assinante recebe as chamadas feitas pelo Publicador.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-402">In the COM+ Events architecture, the subscriber receives the calls made by the publisher.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**objeto de assinatura**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-403"><span id="cos.subscription_object_gloss"></span><span id="COS.SUBSCRIPTION_OBJECT_GLOSS"></span>**subscription object**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-404">No sistema de eventos COM+, um objeto criado por um assinante para solicitar e gerenciar a entrega de eventos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-404">In the COM+ Events system, an object created by a subscriber to request and manage the delivery of events.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**sincronização**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-405"><span id="cos.synchronization_gloss"></span><span id="COS.SYNCHRONIZATION_GLOSS"></span>**synchronization**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-406">No COM+, um serviço que flui de componente para componente e proíbe que mais de um chamador insira o componente em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-406">In COM+, a service that flows from component to component and prohibits more than one caller from entering the component at any given time.</span></span> <span data-ttu-id="3aa2c-407">A sincronização determina quando os threads podem distribuir chamadas para um objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-407">Synchronization determines when threads can dispatch calls to an object.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**modelo de arquitetura de três camadas**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-408"><span id="cos.three_tier_architectural_model_gloss"></span><span id="COS.THREE_TIER_ARCHITECTURAL_MODEL_GLOSS"></span>**three-tier architectural model**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-409">A estrutura fundamental para o modelo de design lógico, segmenta os componentes de um aplicativo em três camadas de serviços da seguinte maneira: a camada de apresentação ou os serviços de usuário; a camada intermediária ou os serviços corporativos; e a camada de dados ou serviços de dados.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-409">The fundamental framework for the logical design model, segments an application's components into three tiers of services as follows: the presentation tier, or user services; the middle tier, or business services; and the data tier, or data services.</span></span> <span data-ttu-id="3aa2c-410">Essas camadas não correspondem necessariamente a locais físicos em vários computadores em uma rede, mas sim a camadas lógicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-410">These tiers do not necessarily correspond to physical locations on various computers on a network, but rather to logical layers of the application.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**evento rigidamente acoplado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-411"><span id="cos.tightly_couple_event_gloss"></span><span id="COS.TIGHTLY_COUPLE_EVENT_GLOSS"></span>**tightly coupled event**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-412">Um evento cujo remetente (Publicador) e destinatário (assinante) estão ligados de forma rigorosa.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-412">An event whose sender (publisher) and receiver (subscriber) are closely bound.</span></span> <span data-ttu-id="3aa2c-413">Em um sistema de eventos rigidamente acoplado, o Publicador é fornecido com uma interface na qual chamar um método quando ocorre uma alteração.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-413">In a tightly coupled event system, the publisher is provided with an interface on which to call a method when a change occurs.</span></span> <span data-ttu-id="3aa2c-414">O assinante sabe para qual editor solicitar notificação e as interfaces que são expostas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-414">The subscriber knows which publisher to request notification from and the interfaces that are exposed.</span></span> <span data-ttu-id="3aa2c-415">Um sistema de eventos firmemente acoplado requer que o Publicador e o assinante estejam em execução o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-415">A tightly coupled event system requires that both the publisher and the subscriber are running at all times.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**log de rastreamento**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-416"><span id="cos.trace_log_gloss"></span><span id="COS.TRACE_LOG_GLOSS"></span>**trace log**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-417">Um arquivo de log gerado automaticamente pelo Microsoft Coordenador de Transações Distribuídas que mostra os dados relacionados a uma ou mais transações distribuídas.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-417">A log file automatically generated by the Microsoft Distributed Transaction Coordinator that shows data related to one or more distributed transactions.</span></span> <span data-ttu-id="3aa2c-418">Exemplos de dados em um log de rastreamento são ID da transação, tempo da transação e mensagens que indicam o resultado da transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-418">Examples of data in a trace log are transaction ID, transaction time, and messages indicating the transaction outcome.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**aciona**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-419"><span id="cos.transaction_gloss"></span><span id="COS.TRANSACTION_GLOSS"></span>**transaction**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-420">Uma unidade de trabalho na qual uma série de operações relacionadas ocorre durante um processo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-420">A unit of work in which a series of related operations occur during an application process.</span></span> <span data-ttu-id="3aa2c-421">Uma transação é executada exatamente uma vez e é atômica – qualquer trabalho é feito ou nenhum deles é.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-421">A transaction executes exactly once and is atomic—either all of the work is done or none of it is.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Protocolo TIP (Transaction Internet Protocol)**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-422"><span id="cos.transaction_internet_protocol_gloss"></span><span id="COS.TRANSACTION_INTERNET_PROTOCOL_GLOSS"></span>**Transaction Internet Protocol (TIP)**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-423">O protocolo de Internet de transação é um protocolo de confirmação padrão de duas fases que permite que os gerenciadores de transações heterogêneas coordenem transações distribuídas, especialmente pela Internet.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-423">Transaction Internet Protocol is a standard two-phase commit protocol that enables heterogeneous transaction managers to coordinate distributed transactions, especially over the Internet.</span></span> <span data-ttu-id="3aa2c-424">O protocolo TIP de confirmação de duas fases é simples de implementar e é independente do protocolo de comunicação entre aplicativos, de modo que ele possa ser usado com qualquer protocolo de aplicativo, mas especialmente HTTP.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-424">The TIP two-phase commit protocol is simple to implement and is independent of the application-to-application communications protocol, such that it may be used with any application protocol but especially HTTP.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**Gerenciador de transações**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-425"><span id="cos.transaction_manager_gloss"></span><span id="COS.TRANSACTION_MANAGER_GLOSS"></span>**transaction manager**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-426">A parte do Microsoft Coordenador de Transações Distribuídas (DTC) que é executada em cada computador que participa de uma transação distribuída e gerencia as atividades relacionadas à confirmação ou anulação dessa parte da transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-426">The part of the Microsoft Distributed Transaction Coordinator (DTC) that executes on each computer participating in a distributed transaction and manages the activities related to committing or aborting that part of the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**aplicativo de processamento de transações**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-427"><span id="cos.transaction_processing_application_gloss"></span><span id="COS.TRANSACTION_PROCESSING_APPLICATION_GLOSS"></span>**transaction processing application**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-428">Uma coleção de operações de transação que automatiza uma determinada tarefa de negócios.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-428">A collection of transaction operations that automate a given business task.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**sistema de processamento de transações**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-429"><span id="cos.transaction_processing_system_gloss"></span><span id="COS.TRANSACTION_PROCESSING_SYSTEM_GLOSS"></span>**transaction processing system**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-430">Um sistema completo, composto por hardware e software do computador, que hospeda um aplicativo de processamento de transações para executar transações rotineiras necessárias para realizar negócios.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-430">A complete system, comprising both computer hardware and software, that hosts a transaction processing application to perform routine transactions necessary to conduct business.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**Protocolo de confirmação de duas fases**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-431"><span id="cos.two_phase_commit_protocol_gloss"></span><span id="COS.TWO_PHASE_COMMIT_PROTOCOL_GLOSS"></span>**two-phase commit protocol**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-432">Um protocolo usado somente em transações distribuídas, garante que o resultado de uma transação seja consistente em todos os gerenciadores de transações que participam da transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-432">A protocol used only in distributed transactions, ensures that the outcome of a transaction is consistent across all transaction managers participating in the transaction.</span></span> <span data-ttu-id="3aa2c-433">O protocolo opera em duas fases distintas para, por fim, confirmar ou anular uma transação: a fase 1 avalia a condição de cada Gerenciador de recursos e a fase dois conclui a transação.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-433">The protocol operates in two distinct phases to ultimately commit or abort a transaction: phase one evaluates the condition of each resource manager, and phase two completes the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**componente não configurado**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-434"><span id="cos.unconfigured_component_gloss"></span><span id="COS.UNCONFIGURED_COMPONENT_GLOSS"></span>**unconfigured component**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-435">Um componente COM que não foi configurado no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-435">A COM component that has not been configured within the COM+ catalog.</span></span> <span data-ttu-id="3aa2c-436">Os componentes não configurados não podem fazer uso de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-436">Unconfigured components cannot make use of COM+ services.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**localização**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-437"><span id="cos.whereabouts_gloss"></span><span id="COS.WHEREABOUTS_GLOSS"></span>**whereabouts**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-438">Para transações do DTC, uma estrutura de dados opaca que representa o endereço do Gerenciador de transações do Gerenciador de recursos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-438">For DTC transactions, an opaque data structure that represents the address of the resource manager's transaction manager.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**Interfaces XA**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-439"><span id="cos.xa_interfaces_gloss"></span><span id="COS.XA_INTERFACES_GLOSS"></span>**XA interfaces**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-440">Um conjunto padrão de interfaces de programação que permite que os desenvolvedores de aplicativos COM+ acessem bancos de dados compatíveis com XA e criem gerenciadores de recursos que operam com bancos de dados relacionais, Enfileiramento de mensagens, arquivos transacionais e bancos de dados orientados a objeto.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-440">A standard set of programming interfaces that allow COM+ application developers to access XA-compliant databases and create resource managers that operate with relational databases, message queuing, transactional files, and object-oriented databases.</span></span> <span data-ttu-id="3aa2c-441">Embora a Microsoft não ofereça suporte direto ao protocolo XA, a Microsoft oferece suporte a recursos de conversão entre transações OLE e XA.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-441">Although Microsoft does not directly support the XA protocol, Microsoft does support translation facilities between OLE transactions and XA.</span></span>

</dd> <dt>

<span data-ttu-id="3aa2c-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**Serviços Web XML**</span><span class="sxs-lookup"><span data-stu-id="3aa2c-442"><span id="cos.xml_web_services_gloss"></span><span id="COS.XML_WEB_SERVICES_GLOSS"></span>**XML web services**</span></span>
</dt> <dd>

<span data-ttu-id="3aa2c-443">Unidades de lógica do aplicativo que fornecem dados e serviços para outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-443">Units of application logic providing data and services to other applications.</span></span> <span data-ttu-id="3aa2c-444">Os aplicativos acessam serviços Web XML por meio de protocolos Web padrão, como SOAP.</span><span class="sxs-lookup"><span data-stu-id="3aa2c-444">Applications access XML web services through standard Web protocols, such as SOAP.</span></span>

</dd> </dl>

 

 
