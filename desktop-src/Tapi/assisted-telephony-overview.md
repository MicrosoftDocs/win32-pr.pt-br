---
description: Um recurso valioso de telefonia é o pequeno conjunto de funções chamadas de telefonia assistida.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Visão geral de telefonia assistida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6a8826fd0c273936204d9250fb91504333d807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922090"
---
# <a name="assisted-telephony-overview"></a>Visão geral de telefonia assistida

Um recurso valioso de telefonia é o pequeno conjunto de funções chamadas de telefonia assistida. A telefonia assistida foi projetada para fazer o estabelecimento de chamadas de voz e de chamadas de mídia disponíveis para qualquer aplicativo, não apenas aquelas dedicadas à funcionalidade de telefonia. Em outras palavras, a telefonia assistida permite que os aplicativos façam chamadas telefônicas sem a necessidade de estar atento aos detalhes dos serviços da API de telefonia completa. Ele estende a telefonia para aplicativos de processamento de texto, planilhas, bancos de dados, gerenciadores de informações pessoais e outros aplicativos sem telefonia.

Para obter uma lista de funções de telefonia assistidas da TAPI 2. x de telefonia básica, consulte [referência de função rápida TAPI](./tapi-quick-function-reference.md). A TAPI 3. x dá suporte à telefonia assistida por meio da interface [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) .

A utilidade da telefonia assistida pode ser ilustrada pelo exemplo a seguir. Um aplicativo de planilha pode incorporar funções que discam um número de telefone para uma chamada de fala. Desde que o aplicativo não precise de nenhum controle de chamada detalhado fornecido pela API de telefonia completa, a telefonia assistida é a maneira mais fácil e eficiente de fornecer a funcionalidade de telefonia.

![telefonia assistida com um aplicativo de planilha](images/assist4.png)

A telefonia assistida e a API de telefonia completa são usadas e implementadas de maneiras diferentes, portanto, não é recomendável misturar chamadas de função de telefonia assistidas e chamadas de função de API de telefonia em um único aplicativo.

## <a name="using-assisted-telephony"></a>Usando a telefonia assistida

Os aplicativos que usam serviços de telefonia assistida iniciam apenas solicitações de chamada que são enfileiradas temporariamente pela TAPI. O aplicativo destinatário da solicitação recupera essas solicitações e as executa em nome do aplicativo de telefonia assistido. A função [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita o estabelecimento de uma chamada de voz. O aplicativo solicitante não controla a chamada.

A TAPI permite que o usuário estabeleça diferentes ou os mesmos aplicativos de destinatário de solicitação para cada um desses serviços. Um aplicativo torna-se um destinatário de solicitação registrando-se com [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), em que **true** é especificado como o valor para o parâmetro *bEnable*. (A especificação de **false** cancela o registro do aplicativo como um destinatário da solicitação, que deve ser feito quando determinou que suas tarefas de destinatário estão por meio da sessão atual.) O aplicativo seleciona os serviços que deseja manipular no parâmetro *dwRequestMode* de **lineRegisterRequestRecipient**. Um valor possível para uma solicitação é LINEREQUESTMODE \_ MAKECALL, para mostrar que o aplicativo tratará as solicitações [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) . Se vários aplicativos se registrarem para os mesmos serviços, um esquema de prioridade será usado para permitir que o usuário selecione qual aplicativo é preferencial para lidar com solicitações. Esse esquema de prioridade é idêntico ao usado para a entrega de chamada e o roteamento de chamadas de entrada com base em uma lista de nomes de arquivo em **HandoffPriorities** no registro.

## <a name="call-requests"></a>Solicitações de chamada

A telefonia assistida fornece aplicativos habilitados para telefonia com um mecanismo fácil de usar para fazer chamadas telefônicas sem exigir que o desenvolvedor se torne totalmente compensante em telefonia.

A função [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita uma chamada de voz entre o usuário e uma parte remota especificada por seu número de telefone. A solicitação é feita à TAPI, que a transmite para um aplicativo que é registrado como um destinatário dessas solicitações. Esse destinatário é um aplicativo do Gerenciador de chamadas.

Depois que o aplicativo tiver feito a solicitação, a chamada será controlada inteiramente do aplicativo do Gerenciador de chamadas, porque os aplicativos de telefonia assistida não podem gerenciar chamadas. Como os aspectos mais complexos de telefonia e todas as operações de interface do usuário são tratados pelo aplicativo do Gerenciador de chamadas, os aplicativos habilitados para telefonia não precisam ser modificados de forma substancial. Na verdade, os aplicativos que permitem que essa operação seja invocada de sua linguagem de script interna talvez não precisem ser modificados.

A função [**tapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) retorna para o aplicativo o código de país ou região e o código de cidade (área) que o usuário definiu nos parâmetros do local atual no painel de controle de telefonia. O aplicativo pode usar essas informações para ajudar o usuário a formar números de telefone canônicos adequados, por exemplo, oferecendo esses valores como padrões quando novos números são inseridos em uma entrada de catálogo telefônico ou registro de banco de dados.

## <a name="request-recipients"></a>Solicitar destinatários

Dois tipos de aplicativos são necessários para executar a telefonia assistida. *Clientes* de telefonia assistida são aplicativos que usam telefonia assistida chamando as funções que têm o prefixo "TAPI". Um exemplo de tal aplicativo cliente seria uma planilha à qual um comando de menu de **discagem** ou botão de barra de ferramentas é adicionado.

Os *servidores* de telefonia assistida são aplicativos que podem executar funções de API de telefonia que resultam da chamada de outro aplicativo para uma função prefixada "TAPI". Para se tornar conhecido como um servidor de telefonia assistido, tal aplicativo é registrado como um usando a função [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) .

As funções de telefonia assistida (que começam com o prefixo "TAPI") são conhecidas como *funções de solicitação*. Os aplicativos de telefonia assistida que processam essas solicitações — servidores de telefonia assistida — são chamados de *destinatários de solicitação*.

## <a name="processing-assisted-telephony-requests"></a>Processando solicitações de telefonia assistidas

O processo com o qual as solicitações são entregues e é atendido é o seguinte:

1.  Quando a TAPI recebe uma solicitação de telefonia assistida, ela verifica se há um destinatário de solicitação, ou seja, um aplicativo atualmente registrado para processar esse tipo de solicitação. Se houver um destinatário de solicitação, a solicitação será enfileirada e o aplicativo de prioridade mais alta que foi registrado para o serviço da solicitação será enviado uma mensagem de [**\_ solicitação de linha**](./line-request.md) . A mensagem notifica o destinatário da solicitação de que uma nova solicitação chegou e transporta uma indicação do modo da solicitação.
2.  Se a TAPI não puder encontrar um aplicativo em execução no momento para processar essa solicitação, ele tentará iniciar um aplicativo que tenha sido registrado como sendo capaz de fazer isso. Essas informações de registro são registradas em **HandoffPriorities** no registro. A TAPI tenta iniciar aplicativos na ordem em que estão listados na seção **HandoffPriorities** . (Consulte a etapa a seguir.)

    Se nenhum aplicativo estiver registrado no momento, a TAPI examinará a lista de aplicativos de processamento de solicitações na entrada associada no **HandoffPriorities**. Se a linha associada estiver ausente no arquivo, se não houver nenhum aplicativo listado nela, ou se nenhum dos aplicativos na lista puder ser iniciado, a solicitação será rejeitada com o erro TAPIERR \_ NOREQUESTRECIPIENT.

    Quando um destinatário de solicitação é iniciado (quer ele tenha sido iniciado pela TAPI), é sua obrigação chamar [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) durante o processo de inicialização e se registrar como um destinatário de solicitação.

3.  Se um ou mais aplicativos estiverem listados na entrada, a TAPI começará com o primeiro aplicativo listado (prioridade mais alta) e tentará iniciá-lo usando a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Se a tentativa de iniciar o aplicativo falhar, a TAPI tentará iniciar o próximo aplicativo na lista. Quando qualquer aplicativo é iniciado com êxito, a TAPI simplesmente enfileira a solicitação e retorna uma indicação de êxito para o aplicativo, embora a solicitação ainda não tenha sido sinalizada para o destinatário da solicitação.

    Depois que o aplicativo destinatário da solicitação é iniciado, ele chama [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), que faz com que uma mensagem de [**\_ solicitação de linha**](./line-request.md) seja enviada, sinalizando que a solicitação está na fila. Se, por algum motivo, o aplicativo iniciado nunca se registrar, a solicitação permanecerá na fila e permanecerá na fila indefinidamente até que um aplicativo seja registrado para esse tipo de solicitação.

4.  Se a TAPI encontrar esse aplicativo registrado já em execução ou iniciar com êxito um, ele enfileirará a solicitação, enviando uma mensagem de solicitação de linha \_ para o aplicativo de servidor e retornará uma indicação de êxito para a chamada de função para o aplicativo de telefonia assistido. Essa mensagem de êxito indica apenas que a solicitação foi aceita e enfileirada, não que tenha sido executada com êxito.

Quando o aplicativo de servidor está pronto para processar uma solicitação, ele chama a função [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) . Isso permite que ele receba todas as informações necessárias, como um endereço para discagem. Em seguida, ele processa a solicitação, usando as funções TAPI (como [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) e [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)) que, de outra forma, seriam usadas para fazer a chamada. Invocar **lineGetRequest** remove a solicitação da TAPI e os parâmetros de solicitação são copiados em um buffer de solicitação alocado pelo aplicativo. O tamanho e a interpretação do conteúdo do buffer dependem do modo de solicitação.

O servidor deve garantir que ele use os parâmetros corretos ao executar solicitações. Ao fazer isso, estas etapas são seguidas:

1.  O destinatário da solicitação recebe primeiro uma mensagem de [**\_ solicitação de linha**](./line-request.md) informando que as solicitações podem existir para ela na fila de solicitações. Isso diz ao aplicativo para chamar [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) e continuar chamando-o até que a fila seja drenada (se a solicitação for para fazer uma nova chamada) ou para remover uma chamada existente. Essa mensagem não contém os parâmetros para a solicitação, exceto no caso de uma solicitação para remover uma chamada existente.
2.  Se a solicitação for fazer uma nova chamada, o servidor de telefonia assistido usará a função [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) para recuperar a solicitação completa, que inclui os parâmetros da solicitação. O servidor agora tem todas as informações de que precisa, como o número a ser discado ou a identificação do criador da solicitação. No entanto, primeiro o servidor deve alocar a memória necessária para armazenar essas informações.
3.  Por fim, o servidor executa a solicitação invocando a função TAPI apropriada ou o conjunto de funções.

Se a TAPI não puder iniciar um aplicativo capaz de servir como um destinatário de solicitação, a chamada de telefonia assistida falhará e retornará o erro TAPIERR \_ NOREQUESTRECIPIENT.

## <a name="notes-on-request-recipient-operations"></a>Observações sobre operações de destinatário da solicitação

As informações a seguir referem-se aos sistemas nos quais as solicitações de telefonia assistidas são processadas:

-   O registro padrão deve listar um aplicativo do Gerenciador de chamadas na lista de prioridade para [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall). Seria útil, mas não essencial, para que o aplicativo do Gerenciador de chamadas tenha uma opção de menu que permita aos usuários defini-lo com a prioridade mais alta.
-   Quando um aplicativo de destinatário de telefonia assistido é iniciado automaticamente pela TAPI e se é o único aplicativo TAPI no sistema, essa ação Inicializa a TAPI. Se o aplicativo de destinatário de telefonia assistido inicializar e desligar o dispositivo de linha antes de se registrar para solicitações de telefonia assistidas, a TAPI também será desligada e a solicitação de telefonia assistida será perdida. As solicitações de telefonia assistidas também podem ser perdidas quando outro aplicativo TAPI que é iniciado executa uma inicialização e um desligamento.

 

 
