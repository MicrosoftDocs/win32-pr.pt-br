---
description: O moniker da fila é usado para ativar um componente enfileirado programaticamente.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Usando o moniker da fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 228964157d08aca868474167ae16590692f16ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784528"
---
# <a name="using-the-queue-moniker"></a><span data-ttu-id="67ca4-103">Usando o moniker da fila</span><span class="sxs-lookup"><span data-stu-id="67ca4-103">Using the Queue Moniker</span></span>

<span data-ttu-id="67ca4-104">O moniker da fila é usado para ativar um componente enfileirado programaticamente.</span><span class="sxs-lookup"><span data-stu-id="67ca4-104">The queue moniker is used to activate a queued component programmatically.</span></span> <span data-ttu-id="67ca4-105">O moniker da fila requer que ele receba a ID da classe (CLSID) do objeto a ser invocado do novo moniker diretamente à direita dele.</span><span class="sxs-lookup"><span data-stu-id="67ca4-105">The queue moniker requires that it receive the class ID (CLSID) of the object to be invoked from the new moniker directly to the right of it.</span></span> <span data-ttu-id="67ca4-106">Quando prefixado à esquerda, o novo moniker passa o CLSID para o moniker à esquerda dele.</span><span class="sxs-lookup"><span data-stu-id="67ca4-106">When left-prefixed, the new moniker passes the CLSID to the moniker to the left of it.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="67ca4-107">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="67ca4-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="67ca4-108">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="67ca4-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="67ca4-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="67ca4-109">Visual Basic</span></span>

<span data-ttu-id="67ca4-110">O parâmetro de nome de exibição GetObject é "Queue:/novo:", seguido da ID do programa ou do GUID do formato de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-110">The GetObject display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="67ca4-111">Os exemplos a seguir mostram três ativações válidas de um componente com o moniker da fila:</span><span class="sxs-lookup"><span data-stu-id="67ca4-111">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a><span data-ttu-id="67ca4-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="67ca4-112">C/C++</span></span>

<span data-ttu-id="67ca4-113">O parâmetro nome de exibição do [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) é "fila:/novo:", seguido da ID do programa ou do GUID do formato de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-113">The [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) display name parameter is "queue:/new:", followed by the program ID or string-form GUID, with or without braces, of the server object to be instantiated.</span></span> <span data-ttu-id="67ca4-114">Os exemplos a seguir mostram três ativações válidas de um componente com o moniker da fila:</span><span class="sxs-lookup"><span data-stu-id="67ca4-114">The following examples show three valid activations of a component with the queue moniker:</span></span>

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a><span data-ttu-id="67ca4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ca4-115">Remarks</span></span>

<span data-ttu-id="67ca4-116">O moniker da fila aceita parâmetros opcionais que alteram as propriedades da mensagem enviada ao enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-116">The queue moniker accepts optional parameters that alter the properties of the message sent to Message Queuing.</span></span> <span data-ttu-id="67ca4-117">Por exemplo, para fazer com que a mensagem de enfileiramento de mensagens seja enviada com uma prioridade 6, o componente em fila seria ativado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="67ca4-117">For example, to cause the Message Queuing message to be sent with a priority 6, the queued component would be activated as follows:</span></span>

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

<span data-ttu-id="67ca4-118">A tabela a seguir lista os parâmetros de moniker da fila que afetam a fila de destino.</span><span class="sxs-lookup"><span data-stu-id="67ca4-118">The following table lists the queue moniker parameters that affect the destination queue.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67ca4-119">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="67ca4-119">Parameter</span></span></th>
<th><span data-ttu-id="67ca4-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ca4-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67ca4-121"><em>ComputerName</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-121"><em>ComputerName</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-122">Especifica a parte do nome do computador de um nome de caminho da fila do enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-122">Specifies the computer name portion of a Message Queuing queue path name.</span></span> <span data-ttu-id="67ca4-123">O nome do caminho da fila do enfileiramento de mensagens é formatado como <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="67ca4-123">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="67ca4-124">Se não for especificado, o nome do computador associado ao aplicativo configurado será usado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-124">If not specified, the computer name associated with the configured application is used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-125"><em>QueueName</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-125"><em>QueueName</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-126">Especifica o nome da fila do serviço de enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-126">Specifies the Message Queuing queue name.</span></span> <span data-ttu-id="67ca4-127">O nome do caminho da fila do enfileiramento de mensagens é formatado como <em>ComputerName</em> \ <em>QueueName</em>.</span><span class="sxs-lookup"><span data-stu-id="67ca4-127">The Message Queuing queue path name is formatted as <em>ComputerName</em>\<em>QueueName</em>.</span></span> <span data-ttu-id="67ca4-128">Se não for especificado, o nome da fila associado ao aplicativo configurado será usado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-128">If not specified, the queue name associated with the configured application is used.</span></span><br/> <span data-ttu-id="67ca4-129">Para obter uma fila não transacional, você pode especificar o nome da fila primeiro e, em seguida, criar um aplicativo COM+ com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="67ca4-129">To get a non-transactional queue, you can specify the queue name first and then create a COM+ application of the same name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-130"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-130"><em>PathName</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-131">Especifica o nome completo do caminho da fila do enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-131">Specifies the complete Message Queuing queue path name.</span></span> <span data-ttu-id="67ca4-132">Se não for especificado, o nome do caminho da fila do enfileiramento de mensagens associado ao aplicativo configurado será usado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-132">If not specified, the Message Queuing queue path name associated with the configured application is used.</span></span> <span data-ttu-id="67ca4-133">Para substituir o nome de destino, o caminho pode ser especificado no seguinte formato para uma instalação de grupo de trabalho do enfileiramento de mensagens:</span><span class="sxs-lookup"><span data-stu-id="67ca4-133">To override the destination name, the path can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="67ca4-134">Queue:<em>PathName</em> = <em>ComputerName</em>\Bytes privados $ \ AppName/New: MyProject. CMyClass</span><span class="sxs-lookup"><span data-stu-id="67ca4-134">Queue:<em>PathName</em>=<em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="67ca4-135">As linguagens de programação C e Microsoft Visual C++ exigem duas barras invertidas para representar uma barra invertida em literais de cadeia de caracteres, por exemplo, folha de pagamento de Chicago \\ .</span><span class="sxs-lookup"><span data-stu-id="67ca4-135">Both the C and Microsoft Visual C++ programming languages require two backslashes to represent one backslash within string literals for example, chicago\\payroll.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-136"><em>FormatName</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-136"><em>FormatName</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-137">Quando você marca um aplicativo COM+ como enfileirado, o COM+ cria uma fila de enfileiramento de mensagens cujo nome é o mesmo que o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67ca4-137">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="67ca4-138">O nome do formato de enfileiramento de mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="67ca4-138">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="67ca4-139">Para substituir o nome de destino, o nome do formato pode ser especificado no seguinte formato para uma instalação do grupo de trabalho do enfileiramento de mensagens:</span><span class="sxs-lookup"><span data-stu-id="67ca4-139">To override the destination name, the format name can be specified in the following form for a Message Queuing workgroup installation:</span></span><br/> <span data-ttu-id="67ca4-140">Fila:<em>FormatName</em>= Direct = os:<em>ComputerName</em>\Bytes privados $ \ AppName/New: ProgID</span><span class="sxs-lookup"><span data-stu-id="67ca4-140">Queue:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId</span></span><br/> <span data-ttu-id="67ca4-141">Em uma configuração de Active Directory, &quot; Private $ &quot; não é especificado como parte do nome da fila.</span><span class="sxs-lookup"><span data-stu-id="67ca4-141">In an Active Directory configuration, &quot;PRIVATE$&quot; is not specified as part of the queue name.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="67ca4-142">Os parâmetros de moniker de fila opcionais são processados da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="67ca4-142">Optional queue moniker parameters are processed left-to-right.</span></span> <span data-ttu-id="67ca4-143">Especifique cada palavra-chave apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="67ca4-143">Specify each keyword only one time.</span></span> <span data-ttu-id="67ca4-144">A especificação do parâmetro *PathName* substitui os parâmetros *ComputerName* e *QueueName*.</span><span class="sxs-lookup"><span data-stu-id="67ca4-144">Specifying the *PathName* parameter replaces both the *ComputerName* and *QueueName* parameters.</span></span> <span data-ttu-id="67ca4-145">Um parâmetro *FormatName* específico exclui o conhecimento prévio de um parâmetro *ComputerName*, *QueueName* e *PathName* .</span><span class="sxs-lookup"><span data-stu-id="67ca4-145">A specific *FormatName* parameter deletes prior knowledge of a *ComputerName*, *QueueName*, and *PathName* parameter.</span></span>

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a><span data-ttu-id="67ca4-146">Associando o ouvinte de componentes na fila a uma fila particular específica</span><span class="sxs-lookup"><span data-stu-id="67ca4-146">Associating the Queued Components Listener with a Specific Private Queue</span></span>

<span data-ttu-id="67ca4-147">O ouvinte de componentes na fila COM+ recebe somente de filas associadas ao aplicativo COM+ marcado como enfileirado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-147">The COM+ Queued Components listener receives only from queues associated with the COM+ application marked queued.</span></span> <span data-ttu-id="67ca4-148">Quando você marca um aplicativo COM+ como enfileirado, o COM+ cria uma fila de enfileiramento de mensagens cujo nome é o mesmo que o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67ca4-148">When you mark a COM+ application as queued, COM+ creates a Message Queuing queue whose name is the same as the application.</span></span> <span data-ttu-id="67ca4-149">O nome do formato de enfileiramento de mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="67ca4-149">The Message Queuing format name of that queue is in the COM+ catalog, associated with the COM+ application.</span></span> <span data-ttu-id="67ca4-150">Quando o aplicativo COM+ é iniciado e marcado como escuta, um ouvinte no processo do aplicativo COM+ é iniciado e a fila é aberta.</span><span class="sxs-lookup"><span data-stu-id="67ca4-150">When the COM+ application is started and marked as listen, a listener in the COM+ application process is started and the queue is opened.</span></span> <span data-ttu-id="67ca4-151">A tabela a seguir lista os parâmetros de moniker da fila que afetam a mensagem do serviço de enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-151">The following table lists the queue moniker parameters that affect the Message Queuing message.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67ca4-152">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="67ca4-152">Parameter</span></span></th>
<th><span data-ttu-id="67ca4-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="67ca4-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67ca4-154"><em>AppSpecific</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-154"><em>AppSpecific</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-155">Especifica um inteiro sem sinal, por exemplo, AppSpecific = 12345.</span><span class="sxs-lookup"><span data-stu-id="67ca4-155">Specifies an unsigned integer for example, AppSpecific=12345.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-156"><em>AuthLevel</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-156"><em>AuthLevel</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-157">Especifica o nível de autenticação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="67ca4-157">Specifies the message authentication level.</span></span> <span data-ttu-id="67ca4-158">Uma mensagem autenticada é assinada digitalmente e requer um certificado para o usuário que está enviando a mensagem.</span><span class="sxs-lookup"><span data-stu-id="67ca4-158">An authenticated message is digitally signed and requires a certificate for the user sending the message.</span></span> <span data-ttu-id="67ca4-159">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-159">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-160">MQMSG_AUTH_LEVEL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-160">MQMSG_AUTH_LEVEL_NONE,0</span></span></li>
<li><span data-ttu-id="67ca4-161">MQMSG_AUTH_LEVEL_ALWAYS, 1</span><span class="sxs-lookup"><span data-stu-id="67ca4-161">MQMSG_AUTH_LEVEL_ALWAYS,1</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-162"><em>Entrega</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-162"><em>Delivery</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-163">Especifica a opção de entrega de mensagem.</span><span class="sxs-lookup"><span data-stu-id="67ca4-163">Specifies the message delivery option.</span></span> <span data-ttu-id="67ca4-164">Esse valor é ignorado para filas transacionais.</span><span class="sxs-lookup"><span data-stu-id="67ca4-164">This value is ignored for transactional queues.</span></span> <span data-ttu-id="67ca4-165">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-165">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-166">MQMSG_DELIVERY_EXPRESS, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-166">MQMSG_DELIVERY_EXPRESS,0</span></span></li>
<li><span data-ttu-id="67ca4-167">MQMSG_DELIVERY_RECOVERABLE, 1</span><span class="sxs-lookup"><span data-stu-id="67ca4-167">MQMSG_DELIVERY_RECOVERABLE,1</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-168"><em>EncryptAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-168"><em>EncryptAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-169">Especifica o algoritmo de criptografia a ser usado pelo enfileiramento de mensagens para criptografar e descriptografar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="67ca4-169">Specifies the encryption algorithm to be used by Message Queuing to encrypt and decrypt the message.</span></span> <span data-ttu-id="67ca4-170">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-170">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-171">CALG_RC2, CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="67ca4-171">CALG_RC2, CALG_RC4</span></span></li>
<li><span data-ttu-id="67ca4-172">Qualquer valor inteiro aceitável para o enfileiramento de mensagens para um <em>EncryptAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="67ca4-172">Any integer value that is acceptable to Message Queuing for an <em>EncryptAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-173"><em>HashAlgorithm</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-173"><em>HashAlgorithm</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-174">Especifica uma função de hash criptográfico.</span><span class="sxs-lookup"><span data-stu-id="67ca4-174">Specifies a cryptographic hash function.</span></span> <span data-ttu-id="67ca4-175">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-175">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="67ca4-176">CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</span></span></li>
<li><span data-ttu-id="67ca4-177">Qualquer valor inteiro aceitável para o enfileiramento de mensagens para um <em>HashAlgorithm</em>.</span><span class="sxs-lookup"><span data-stu-id="67ca4-177">Any integer value that is acceptable to Message Queuing for a <em>HashAlgorithm</em>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-178">Diário</span><span class="sxs-lookup"><span data-stu-id="67ca4-178">Journal</span></span><br/></td>
<td><span data-ttu-id="67ca4-179">Especifica a opção de diário de mensagens do enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-179">Specifies the Message Queuing message journal option.</span></span> <span data-ttu-id="67ca4-180">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-180">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-181">MQMSG_JOURNAL_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-181">MQMSG_JOURNAL_NONE,0</span></span></li>
<li><span data-ttu-id="67ca4-182">MQMSG_DEADLETTER, 1</span><span class="sxs-lookup"><span data-stu-id="67ca4-182">MQMSG_DEADLETTER,1</span></span></li>
<li><span data-ttu-id="67ca4-183">MQMSG_JOURNAL, 2</span><span class="sxs-lookup"><span data-stu-id="67ca4-183">MQMSG_JOURNAL,2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-184"><em>Rótulo</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-184"><em>Label</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-185">Especifica uma cadeia de caracteres de rótulo de mensagem com até MQ_MAX_MSG_LABEL_LEN caracteres.</span><span class="sxs-lookup"><span data-stu-id="67ca4-185">Specifies a message label string up to MQ_MAX_MSG_LABEL_LEN characters.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-186"><em>MaxTimeToReachQueue</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-186"><em>MaxTimeToReachQueue</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-187">Especifica um tempo máximo, em segundos, para a mensagem chegar à fila.</span><span class="sxs-lookup"><span data-stu-id="67ca4-187">Specifies a maximum time, in seconds, for the message to reach the queue.</span></span> <br/> <span data-ttu-id="67ca4-188">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-188">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-189">INFINITE</span><span class="sxs-lookup"><span data-stu-id="67ca4-189">INFINITE</span></span></li>
<li><span data-ttu-id="67ca4-190">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="67ca4-190">LONG_LIVED</span></span></li>
<li><span data-ttu-id="67ca4-191">Número de segundos</span><span class="sxs-lookup"><span data-stu-id="67ca4-191">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-192"><em>MaxTimeToReceive</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-192"><em>MaxTimeToReceive</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-193">Especifica um tempo máximo, em segundos, para a mensagem a ser recebida pelo aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="67ca4-193">Specifies a maximum time, in seconds, for the message to be received by the target application.</span></span> <span data-ttu-id="67ca4-194">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-194">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-195">INFINITE</span><span class="sxs-lookup"><span data-stu-id="67ca4-195">INFINITE</span></span></li>
<li><span data-ttu-id="67ca4-196">LONG_LIVED</span><span class="sxs-lookup"><span data-stu-id="67ca4-196">LONG_LIVED</span></span></li>
<li><span data-ttu-id="67ca4-197">Número de segundos</span><span class="sxs-lookup"><span data-stu-id="67ca4-197">Number of seconds</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-198"><em>Prioridade</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-198"><em>Priority</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-199">Especifica um nível de prioridade de mensagem, dentro dos valores de enfileiramento de mensagens permitidos.</span><span class="sxs-lookup"><span data-stu-id="67ca4-199">Specifies a message priority level, within the Message Queuing values permitted.</span></span><br/> <span data-ttu-id="67ca4-200">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-200">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-201">MQ_MIN_PRIORITY, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-201">MQ_MIN_PRIORITY,0</span></span></li>
<li><span data-ttu-id="67ca4-202">MQ_MAX_PRIORITY, 7</span><span class="sxs-lookup"><span data-stu-id="67ca4-202">MQ_MAX_PRIORITY,7</span></span></li>
<li><span data-ttu-id="67ca4-203">MQ_DEFAULT_PRIORITY, 3</span><span class="sxs-lookup"><span data-stu-id="67ca4-203">MQ_DEFAULT_PRIORITY,3</span></span></li>
<li><span data-ttu-id="67ca4-204">Número entre 0 e 7</span><span class="sxs-lookup"><span data-stu-id="67ca4-204">Number between 0 and 7</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67ca4-205"><em>PrivLevel</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-205"><em>PrivLevel</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-206">Especifica um nível de privacidade, usado para criptografar mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-206">Specifies a privacy level, used to encrypt messages.</span></span><br/> <span data-ttu-id="67ca4-207">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-207">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-208">MQMSG_PRIV_LEVEL_NONE, NENHUM, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-208">MQMSG_PRIV_LEVEL_NONE, NONE, 0</span></span></li>
<li><span data-ttu-id="67ca4-209">MQMSG_PRIV_LEVEL_BODY, CORPO,</span><span class="sxs-lookup"><span data-stu-id="67ca4-209">MQMSG_PRIV_LEVEL_BODY, BODY,</span></span></li>
<li><span data-ttu-id="67ca4-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span><span class="sxs-lookup"><span data-stu-id="67ca4-210">MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</span></span></li>
<li><span data-ttu-id="67ca4-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span><span class="sxs-lookup"><span data-stu-id="67ca4-211">MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67ca4-212"><em>Rastreou</em></span><span class="sxs-lookup"><span data-stu-id="67ca4-212"><em>Trace</em></span></span><br/></td>
<td><span data-ttu-id="67ca4-213">Especifica as opções de rastreamento, usadas no rastreamento do roteamento de enfileiramento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="67ca4-213">Specifies trace options, used in tracing Message Queuing routing.</span></span><br/> <span data-ttu-id="67ca4-214">Valores aceitáveis:</span><span class="sxs-lookup"><span data-stu-id="67ca4-214">Acceptable values:</span></span><br/>
<ul>
<li><span data-ttu-id="67ca4-215">MQMSG_TRACE_NONE, 0</span><span class="sxs-lookup"><span data-stu-id="67ca4-215">MQMSG_TRACE_NONE,0</span></span></li>
<li><span data-ttu-id="67ca4-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</span><span class="sxs-lookup"><span data-stu-id="67ca4-216">MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="67ca4-217">O conjunto completo de funções SDK administrativas do COM+ está disponível usando objetos COM.</span><span class="sxs-lookup"><span data-stu-id="67ca4-217">The complete set of COM+ Administrative SDK functions is available by using COM objects.</span></span> <span data-ttu-id="67ca4-218">Isso permite que qualquer programa inicie e interrompa aplicativos COM+ conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="67ca4-218">This allows any program to start and stop COM+ applications as required.</span></span>

> [!Note]  
> <span data-ttu-id="67ca4-219">Quando um aplicativo COM+ é iniciado, ele é o aplicativo em execução, e não os componentes individuais dentro do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67ca4-219">When a COM+ application is started, it is the application that is running, not the individual components within the application.</span></span> <span data-ttu-id="67ca4-220">Se um aplicativo chamar um componente não enfileirado, o aplicativo COM+ que contém o componente será iniciado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-220">If an application calls a non-queued component, the COM+ application that contains the component is started.</span></span> <span data-ttu-id="67ca4-221">Se a caixa de seleção ouvinte estiver habilitada, o ouvinte também será iniciado e começará a processar mensagens para componentes enfileirados.</span><span class="sxs-lookup"><span data-stu-id="67ca4-221">If the listener check box is enabled, the listener also starts and begins processing for messages for queued components.</span></span> <span data-ttu-id="67ca4-222">Embora o serviço de componentes na fila possa ser iniciado dessa forma, se você empacotar componentes enfileirados e não enfileirados em um único aplicativo COM+, certifique-se de que você realmente deseja que os componentes na fila sejam iniciados se um componente não enfileirado for executado.</span><span class="sxs-lookup"><span data-stu-id="67ca4-222">While the queued components service can be started in this way, if you package queued and non-queued components into a single COM+ application, be sure that you really want queued components to start if a non-queued component is executed.</span></span> <span data-ttu-id="67ca4-223">Se esse não for o caso, empacote os componentes na fila em um aplicativo COM+ separado dos outros componentes.</span><span class="sxs-lookup"><span data-stu-id="67ca4-223">If this is not the case, package the queued components into a COM+ application that is separate from the other components.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="67ca4-224">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67ca4-224">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67ca4-225">Ativando filas de componentes</span><span class="sxs-lookup"><span data-stu-id="67ca4-225">Activating Component Queues</span></span>](activating-component-queues.md)
</dt> </dl>

 

 




