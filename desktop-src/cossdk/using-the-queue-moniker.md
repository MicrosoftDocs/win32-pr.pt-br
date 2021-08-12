---
description: O moniker da fila é usado para ativar um componente enfileirado programaticamente.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Usando o moniker da fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e83d720478064f1427966de69d98ef06ac82f1da98cc50aa1ec3d3b3ac4c4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305153"
---
# <a name="using-the-queue-moniker"></a>Usando o moniker da fila

O moniker da fila é usado para ativar um componente enfileirado programaticamente. O moniker da fila requer que ele receba a ID da classe (CLSID) do objeto a ser invocado do novo moniker diretamente à direita dele. Quando prefixado à esquerda, o novo moniker passa o CLSID para o moniker à esquerda dele.

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O parâmetro de nome de exibição GetObject é "Queue:/novo:", seguido da ID do programa ou do GUID do formato de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instanciado. Os exemplos a seguir mostram três ativações válidas de um componente com o moniker da fila:

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

O parâmetro nome de exibição do [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) é "fila:/novo:", seguido da ID do programa ou do GUID do formato de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instanciado. Os exemplos a seguir mostram três ativações válidas de um componente com o moniker da fila:

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

## <a name="remarks"></a>Comentários

O moniker da fila aceita parâmetros opcionais que alteram as propriedades da mensagem enviada ao enfileiramento de mensagens. Por exemplo, para fazer com que a mensagem de enfileiramento de mensagens seja enviada com uma prioridade 6, o componente em fila seria ativado da seguinte maneira:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

A tabela a seguir lista os parâmetros de moniker da fila que afetam a fila de destino.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>ComputerName</em><br/></td>
<td>Especifica a parte do nome do computador de um nome de caminho da fila do enfileiramento de mensagens. O nome do caminho da fila do enfileiramento de mensagens é formatado como <em>ComputerName</em> \ <em>QueueName</em>. Se não for especificado, o nome do computador associado ao aplicativo configurado será usado.<br/></td>
</tr>
<tr class="even">
<td><em>QueueName</em><br/></td>
<td>Especifica o nome da fila do serviço de enfileiramento de mensagens. O nome do caminho da fila do enfileiramento de mensagens é formatado como <em>ComputerName</em> \ <em>QueueName</em>. Se não for especificado, o nome da fila associado ao aplicativo configurado será usado.<br/> Para obter uma fila não transacional, você pode especificar o nome da fila primeiro e, em seguida, criar um aplicativo COM+ com o mesmo nome.<br/></td>
</tr>
<tr class="odd">
<td><em>PathName</em><br/></td>
<td>Especifica o nome completo do caminho da fila do enfileiramento de mensagens. Se não for especificado, o nome do caminho da fila do enfileiramento de mensagens associado ao aplicativo configurado será usado. Para substituir o nome de destino, o caminho pode ser especificado no seguinte formato para uma instalação de grupo de trabalho do enfileiramento de mensagens:<br/> Queue:<em>PathName</em> = <em>ComputerName</em>\Bytes privados $ \ AppName/New: MyProject. CMyClass<br/>
<blockquote>
[!Note]<br />
as linguagens de programação C e Microsoft Visual C++ exigem duas barras invertidas para representar uma barra invertida em literais de cadeia de caracteres, por exemplo, folha de pagamento de chicago \\ .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><em>FormatName</em><br/></td>
<td>Quando você marca um aplicativo COM+ como enfileirado, o COM+ cria uma fila de enfileiramento de mensagens cujo nome é o mesmo que o aplicativo. O nome do formato de enfileiramento de mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+. Para substituir o nome de destino, o nome do formato pode ser especificado no seguinte formato para uma instalação do grupo de trabalho do enfileiramento de mensagens:<br/> Fila:<em>FormatName</em>= Direct = os:<em>ComputerName</em>\Bytes privados $ \ AppName/New: ProgID<br/> Em uma configuração de Active Directory, &quot; Private $ &quot; não é especificado como parte do nome da fila. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Os parâmetros de moniker de fila opcionais são processados da esquerda para a direita. Especifique cada palavra-chave apenas uma vez. A especificação do parâmetro *PathName* substitui os parâmetros *ComputerName* e *QueueName*. Um parâmetro *FormatName* específico exclui o conhecimento prévio de um parâmetro *ComputerName*, *QueueName* e *PathName* .

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Associando o ouvinte de componentes na fila a uma fila particular específica

O ouvinte de componentes na fila COM+ recebe somente de filas associadas ao aplicativo COM+ marcado como enfileirado. Quando você marca um aplicativo COM+ como enfileirado, o COM+ cria uma fila de enfileiramento de mensagens cujo nome é o mesmo que o aplicativo. O nome do formato de enfileiramento de mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+. Quando o aplicativo COM+ é iniciado e marcado como escuta, um ouvinte no processo do aplicativo COM+ é iniciado e a fila é aberta. A tabela a seguir lista os parâmetros de moniker da fila que afetam a mensagem do serviço de enfileiramento de mensagens.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>AppSpecific</em><br/></td>
<td>Especifica um inteiro sem sinal, por exemplo, AppSpecific = 12345.<br/></td>
</tr>
<tr class="even">
<td><em>AuthLevel</em><br/></td>
<td>Especifica o nível de autenticação da mensagem. Uma mensagem autenticada é assinada digitalmente e requer um certificado para o usuário que está enviando a mensagem. Valores aceitáveis:<br/>
<ul>
<li>MQMSG_AUTH_LEVEL_NONE, 0</li>
<li>MQMSG_AUTH_LEVEL_ALWAYS, 1</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Entrega</em><br/></td>
<td>Especifica a opção de entrega de mensagem. Esse valor é ignorado para filas transacionais. Valores aceitáveis:<br/>
<ul>
<li>MQMSG_DELIVERY_EXPRESS, 0</li>
<li>MQMSG_DELIVERY_RECOVERABLE, 1</li>
</ul></td>
</tr>
<tr class="even">
<td><em>EncryptAlgorithm</em><br/></td>
<td>Especifica o algoritmo de criptografia a ser usado pelo enfileiramento de mensagens para criptografar e descriptografar a mensagem. Valores aceitáveis:<br/>
<ul>
<li>CALG_RC2, CALG_RC4</li>
<li>Qualquer valor inteiro aceitável para o enfileiramento de mensagens para um <em>EncryptAlgorithm</em>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>HashAlgorithm</em><br/></td>
<td>Especifica uma função de hash criptográfico. Valores aceitáveis:<br/>
<ul>
<li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li>
<li>Qualquer valor inteiro aceitável para o enfileiramento de mensagens para um <em>HashAlgorithm</em>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Diário<br/></td>
<td>Especifica a opção de diário de mensagens do enfileiramento de mensagens. Valores aceitáveis:<br/>
<ul>
<li>MQMSG_JOURNAL_NONE, 0</li>
<li>MQMSG_DEADLETTER, 1</li>
<li>MQMSG_JOURNAL, 2</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Rótulo</em><br/></td>
<td>Especifica uma cadeia de caracteres de rótulo de mensagem com até MQ_MAX_MSG_LABEL_LEN caracteres. <br/></td>
</tr>
<tr class="even">
<td><em>MaxTimeToReachQueue</em><br/></td>
<td>Especifica um tempo máximo, em segundos, para a mensagem chegar à fila. <br/> Valores aceitáveis:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Número de segundos</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>MaxTimeToReceive</em><br/></td>
<td>Especifica um tempo máximo, em segundos, para a mensagem a ser recebida pelo aplicativo de destino. Valores aceitáveis:<br/>
<ul>
<li>INFINITE</li>
<li>LONG_LIVED</li>
<li>Número de segundos</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Prioridade</em><br/></td>
<td>Especifica um nível de prioridade de mensagem, dentro dos valores de enfileiramento de mensagens permitidos.<br/> Valores aceitáveis:<br/>
<ul>
<li>MQ_MIN_PRIORITY,0</li>
<li>MQ_MAX_PRIORITY,7</li>
<li>MQ_DEFAULT_PRIORITY,3</li>
<li>Número entre 0 e 7</li>
</ul></td>
</tr>
<tr class="odd">
<td><em>Privlevel</em><br/></td>
<td>Especifica um nível de privacidade, usado para criptografar mensagens.<br/> Valores aceitáveis:<br/>
<ul>
<li>MQMSG_PRIV_LEVEL_NONE, NONE, 0</li>
<li>MQMSG_PRIV_LEVEL_BODY, BODY,</li>
<li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li>
<li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li>
</ul></td>
</tr>
<tr class="even">
<td><em>Rastreamento</em><br/></td>
<td>Especifica as opções de rastreamento, usadas no rastreamento de roteamento de En en enroscar mensagens.<br/> Valores aceitáveis:<br/>
<ul>
<li>MQMSG_TRACE_NONE,0</li>
<li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li>
</ul></td>
</tr>
</tbody>
</table>



 

O conjunto completo de funções do SDK Administrativo COM+ está disponível usando objetos COM. Isso permite que qualquer programa inicie e pare aplicativos COM+, conforme necessário.

> [!Note]  
> Quando um aplicativo COM+ é iniciado, ele é o aplicativo que está em execução, não os componentes individuais dentro do aplicativo. Se um aplicativo chamar um componente que não está na fila, o aplicativo COM+ que contém o componente será iniciado. Se a caixa de seleção do ouvinte estiver habilitada, o ouvinte também iniciará e iniciará o processamento de mensagens para componentes na fila. Embora o serviço de componentes na fila possa ser iniciado dessa forma, se você empacotar componentes na fila e que não estão na fila em um único aplicativo COM+, certifique-se de que você realmente deseja que os componentes na fila sejam iniciados se um componente que não está na fila for executado. Se esse não for o caso, empacote os componentes na fila em um aplicativo COM+ separado dos outros componentes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ativando filas de componentes](activating-component-queues.md)
</dt> </dl>

 

 




