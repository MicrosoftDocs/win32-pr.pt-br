---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005332"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Recupera o status da condição necessária para dar suporte à entrada de fala.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Endereço de uma variável que recebe um dos seguintes valores para a configuração de Estado:



| Valor                                                                               | Descrição                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const não assinada** **status de escuta longa \_ \_ canlistie = 0;**<br/>               | As condições dão suporte à entrada de fala.                                                                                                                                                                                                          |
| const status de escuta **longa sem sinal** **\_ \_ noáudio = 1;**<br/>                 | Não há nenhum dispositivo de entrada de áudio disponível neste sistema. (Observe que isso não detecta se um microfone está instalado; ele só pode detectar se o usuário tem uma placa de som habilitada para entrada devidamente instalada com um driver funcional.) |
| const status de escuta **longa não assinado não** **\_ \_ superior = 2;**<br/>              | Outro cliente é o cliente ativo desse caractere ou o caractere atual não é o mais alto.                                                                                                                                           |
| const status de escuta **longa não assinado** **\_ \_ CANTOPENAUDIO = 3;**<br/>           | O canal de entrada ou saída de áudio está ocupado no momento, outro aplicativo está usando áudio.                                                                                                                                               |
| const status de escuta **longa não assinado** **\_ \_ COULDNTINITIALIZESPEECH = 4;**<br/> | Ocorreu um erro não especificado no processo de inicialização do subsistema de reconhecimento de fala. Isso inclui a possibilidade de que não haja um mecanismo de fala disponível correspondente à configuração de idioma do caractere.                          |
| const status de escuta **longa não assinado** **\_ \_ SPEECHDISABLED = 5;**<br/>          | O usuário desabilitou a entrada de fala na janela Opções de caractere avançadas.                                                                                                                                                              |
| const erro de status de escuta **longa sem sinal** **\_ \_ = 6;**<br/>                   | Ocorreu um erro ao verificar o status de áudio, mas a causa do erro não foi retornada pelo sistema.                                                                                                                                |



 

</dd> </dl>

Essa função permite consultar se as condições atuais dão suporte à entrada de reconhecimento de fala, incluindo o status do dispositivo de áudio. Se seu aplicativo usar o método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , você poderá usar essa função para garantir melhor que a chamada terá sucesso. Chamar esse método também carregará o mecanismo de fala se ele ainda não estiver carregado. No entanto, ele não ativa o modo de escuta.

Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a consulta do status carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala. Ou seja, a chave de escuta está disponível e a dica de escuta é exibível. (A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.

Essa função retorna apenas a configuração para o uso do caractere do aplicativo cliente; a configuração não reflete outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

 

 





