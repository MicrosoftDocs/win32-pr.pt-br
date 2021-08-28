---
description: O moniker de fila é usado para ativar um componente enfileirado programaticamente.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Usando o Moniker de Fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938b4c0c8afc19e953d7f62f17f95bbd63f387e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473682"
---
# <a name="using-the-queue-moniker"></a>Usando o Moniker de Fila

O moniker de fila é usado para ativar um componente enfileirado programaticamente. O moniker de fila exige que ele receba a CLSID (ID de classe) do objeto a ser invocado do novo moniker diretamente à direita dele. Quando prefixado à esquerda, o novo moniker passa o CLSID para o moniker à esquerda dele.

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Não se aplica.

## <a name="visual-basic"></a>Visual Basic

O parâmetro de nome de exibição GetObject é "queue:/new:", seguido pela ID do programa ou GUID de formulário de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instalá-lo. Os exemplos a seguir mostram três ativações válidas de um componente com o moniker de fila:

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

O parâmetro de nome de exibição [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) é "queue:/new:", seguido pela ID do programa ou GUID de formulário de cadeia de caracteres, com ou sem chaves, do objeto de servidor a ser instalá-lo. Os exemplos a seguir mostram três ativações válidas de um componente com o moniker de fila:

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

O moniker de fila aceita parâmetros opcionais que alteram as propriedades da mensagem enviada ao Enfileiramento de Mensagens. Por exemplo, para fazer com que a mensagem de Enluamento de Mensagens seja enviada com uma prioridade 6, o componente na fila será ativado da seguinte forma:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

A tabela a seguir lista os parâmetros de moniker de fila que afetam a fila de destino.




| Parâmetro | Descrição | 
|-----------|-------------|
| <em>ComputerName</em><br /> | Especifica a parte do nome do computador de um nome de caminho da fila de Enfilagem de Mensagens. O nome do caminho da fila do Enfilamento de Mensagens é formatado como <em>ComputerName</em> \<em> </em> QueueName. Se não for especificado, o nome do computador associado ao aplicativo configurado será usado.<br /> | 
| <em>QueueName</em><br /> | Especifica o nome da fila do Enfilão de Mensagens. O nome do caminho da fila do Enfilamento de Mensagens é formatado como <em>ComputerName</em> \<em> </em> QueueName. Se não for especificado, o nome da fila associado ao aplicativo configurado será usado.<br /> Para obter uma fila não transacional, você pode especificar o nome da fila primeiro e, em seguida, criar um aplicativo COM+ com o mesmo nome.<br /> | 
| <em>PathName</em><br /> | Especifica o nome completo do caminho da fila do Enfilamento de Mensagens. Se não for especificado, o nome do caminho da fila de Enfilagem de Mensagens associado ao aplicativo configurado será usado. Para substituir o nome de destino, o caminho pode ser especificado no seguinte formulário para uma instalação de grupo de trabalho do En en enroscamento de mensagens:<br /> Fila:<em>PathName</em> = <em>ComputerName</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br /><blockquote>[!Note]<br />As linguagens de programação C e Microsoft Visual C++ exigem duas malhas invertida para representar uma faixa invertida em literais de cadeia de caracteres, por exemplo, folha de pagamento \\ de Chicago.</blockquote><br /> | 
| <em>Formatname</em><br /> | Quando você marca um aplicativo COM+ como na fila, o COM+ cria uma fila de Enfilagem de Mensagens cujo nome é o mesmo que o aplicativo. O nome do formato de Enfilagem de Mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+. Para substituir o nome de destino, o nome do formato pode ser especificado no seguinte formulário para uma instalação de grupo de trabalho do En en enrosamento de mensagens:<br /> Fila:<em>FormatName</em>=DIRECT=OS:<em>ComputerName</em>\PRIVATE$\AppName/new:ProgId<br /> Em uma configuração do Active Directory, "PRIVATE$" não é especificado como parte do nome da fila. <br /> | 




 

> [!Note]  
> Parâmetros opcionais de moniker de fila são processados da esquerda para a direita. Especifique cada palavra-chave apenas uma vez. Especificar o *parâmetro PathName* substitui os parâmetros *ComputerName* e *QueueName.* Um parâmetro *FormatName* específico exclui o conhecimento prévio de um parâmetro *ComputerName,* *QueueName* e *PathName.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Associando o ouvinte de componentes na fila a uma fila privada específica

O ouvinte componentes em fila COM+ recebe somente de filas associadas ao aplicativo COM+ marcado na fila. Quando você marca um aplicativo COM+ como na fila, o COM+ cria uma fila de Enfilagem de Mensagens cujo nome é o mesmo que o aplicativo. O nome do formato de Enfilagem de Mensagens dessa fila está no catálogo COM+, associado ao aplicativo COM+. Quando o aplicativo COM+ é iniciado e marcado como escuta, um ouvinte no processo de aplicativo COM+ é iniciado e a fila é aberta. A tabela a seguir lista os parâmetros de moniker de fila que afetam a mensagem de Enfileiramento de Mensagens.




| Parâmetro | Descrição | 
|-----------|-------------|
| <em>Appspecific</em><br /> | Especifica um inteiro sem sinal, por exemplo, AppSpecific=12345.<br /> | 
| <em>AuthLevel</em><br /> | Especifica o nível de autenticação de mensagem. Uma mensagem autenticada é assinada digitalmente e requer um certificado para o usuário que está enviando a mensagem. Valores aceitáveis:<br /><ul><li>MQMSG_AUTH_LEVEL_NONE,0</li><li>MQMSG_AUTH_LEVEL_ALWAYS,1</li></ul> | 
| <em>Entrega</em><br /> | Especifica a opção de entrega de mensagem. Esse valor é ignorado para filas transacionais. Valores aceitáveis:<br /><ul><li>MQMSG_DELIVERY_EXPRESS,0</li><li>MQMSG_DELIVERY_RECOVERABLE,1</li></ul> | 
| <em>EncryptAlgorithm</em><br /> | Especifica o algoritmo de criptografia a ser usado pelo En en fila de mensagens para criptografar e descriptografar a mensagem. Valores aceitáveis:<br /><ul><li>CALG_RC2, CALG_RC4</li><li>Qualquer valor inteiro que seja aceitável para o En envelhamento de mensagens para <em>um EncryptAlgorithm.</em></li></ul> | 
| <em>Hashalgorithm</em><br /> | Especifica uma função de hash criptográfico. Valores aceitáveis:<br /><ul><li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li><li>Qualquer valor inteiro que seja aceitável para o En envelhamento de mensagens para <em>um HashAlgorithm</em>.</li></ul> | 
| Diário<br /> | Especifica a opção de diário de mensagem do En en enrosamento de mensagens. Valores aceitáveis:<br /><ul><li>MQMSG_JOURNAL_NONE,0</li><li>MQMSG_DEADLETTER,1</li><li>MQMSG_JOURNAL,2</li></ul> | 
| <em>Rótulo</em><br /> | Especifica uma cadeia de caracteres de rótulo de mensagem até MQ_MAX_MSG_LABEL_LEN caracteres. <br /> | 
| <em>MaxTimeToReachQueue</em><br /> | Especifica um tempo máximo, em segundos, para que a mensagem alcance a fila. <br /> Valores aceitáveis:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Número de segundos</li></ul> | 
| <em>MaxTimeToReceive</em><br /> | Especifica um tempo máximo, em segundos, para que a mensagem seja recebida pelo aplicativo de destino. Valores aceitáveis:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Número de segundos</li></ul> | 
| <em>Prioridade</em><br /> | Especifica um nível de prioridade de mensagem, dentro dos valores permitidos do En enroscamento de mensagens.<br /> Valores aceitáveis:<br /><ul><li>MQ_MIN_PRIORITY, 0</li><li>MQ_MAX_PRIORITY, 7</li><li>MQ_DEFAULT_PRIORITY, 3</li><li>Número entre 0 e 7</li></ul> | 
| <em>PrivLevel</em><br /> | Especifica um nível de privacidade, usado para criptografar mensagens.<br /> Valores aceitáveis:<br /><ul><li>MQMSG_PRIV_LEVEL_NONE, NENHUM, 0</li><li>MQMSG_PRIV_LEVEL_BODY, CORPO,</li><li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li><li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li></ul> | 
| <em>Trace</em><br /> | Especifica as opções de rastreamento, usadas no rastreamento do roteamento de enfileiramento de mensagens.<br /> Valores aceitáveis:<br /><ul><li>MQMSG_TRACE_NONE, 0</li><li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE, 1</li></ul> | 




 

O conjunto completo de funções SDK administrativas do COM+ está disponível usando objetos COM. Isso permite que qualquer programa inicie e interrompa aplicativos COM+ conforme necessário.

> [!Note]  
> Quando um aplicativo COM+ é iniciado, ele é o aplicativo em execução, e não os componentes individuais dentro do aplicativo. Se um aplicativo chamar um componente não enfileirado, o aplicativo COM+ que contém o componente será iniciado. Se a caixa de seleção ouvinte estiver habilitada, o ouvinte também será iniciado e começará a processar mensagens para componentes enfileirados. Embora o serviço de componentes na fila possa ser iniciado dessa forma, se você empacotar componentes enfileirados e não enfileirados em um único aplicativo COM+, certifique-se de que você realmente deseja que os componentes na fila sejam iniciados se um componente não enfileirado for executado. Se esse não for o caso, empacote os componentes na fila em um aplicativo COM+ separado dos outros componentes.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ativando filas de componentes](activating-component-queues.md)
</dt> </dl>

 

 




