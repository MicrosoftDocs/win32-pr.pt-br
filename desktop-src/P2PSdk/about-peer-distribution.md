---
description: A API de distribuição de pares, que dá suporte ao recurso de cache de ramificação no Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012 oferece um conjunto de APIs de plataforma que pode aumentar a capacidade de resposta de rede de aplicativos centralizados quando acessados em escritórios remotos e ajudar a reduzir a utilização geral de WAN (rede de longa distância) sem interferir nas tecnologias de
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Sobre a distribuição de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b9a99a65ea2cfda6dc8ad9accd4d881529e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828420"
---
# <a name="about-peer-distribution"></a>Sobre a distribuição de pares

A API de distribuição de pares, que dá suporte ao recurso de cache de ramificação no Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012 oferece um conjunto de APIs de plataforma que pode aumentar a capacidade de resposta de rede de aplicativos centralizados quando acessados em escritórios remotos e ajudar a reduzir a utilização geral de WAN (rede de longa distância) sem interferir nas tecnologias de

O sistema de distribuição de mesmo nível oferece um conjunto de APIs de plataforma utilizado por ambos os editores que fornecem conteúdo digital e consumidores que o solicitam. Para diferenciar essas funções facilmente, pode ser mais fácil imaginar o Publicador em uma função de servidor e o consumidor em uma função de cliente. Além disso, é importante lembrar que, além dessas funções conceituais, o serviço de distribuição de mesmo nível é um sistema de par verdadeiro, conforme indicado pela capacidade de qualquer nó de distribuição de mesmo nível para publicar e consumir conteúdo digital. As APIs de plataforma de distribuição de pares são expostas a editores e consumidores por uma biblioteca de importação do Win32 (**PeerDist. lib**).

O ciclo de vida do conteúdo fornecido por um Publicador e recuperado por um consumidor com o serviço de distribuição de mesmo nível é composto pelas seguintes operações:



|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Publicação de conteúdo** | A publicação é feita para produzir uma descrição de informações de **conteúdo** com termo de conteúdo ou informações de **conteúdo** de forma abreviada. Essas informações de conteúdo podem ser usadas por uma instância do serviço de distribuição de mesmo nível para autenticar e recriar o conteúdo. Quando o conteúdo é publicado por um aplicativo no serviço de distribuição de mesmo nível, que é conceitualmente uma operação do lado do servidor, esse conteúdo se torna associado à identidade do editor, que é baseada no SID do usuário associado ao token de acesso do thread. Essa associação é feita para limitar o acesso ao conteúdo por entidades não autorizadas. No entanto, é importante observar que o acesso às informações de conteúdo é equivalente ao acesso ao próprio conteúdo, pois as informações de conteúdo podem ser usadas para obter o conteúdo de pares ou de um cache hospedado.<br/> Há uma nova versão da estrutura de dados de informações de conteúdo no Windows 8; no entanto, ainda há suporte para a versão anterior. Para interoperar com clientes do Windows 7, um administrador pode configurar o serviço de distribuição de mesmo nível para usar a versão anterior da estrutura de dados de informações de conteúdo.<br/> |
| **Recuperação de conteúdo**   | Para que um consumidor recupere conteúdo do serviço de distribuição de mesmo nível, o acesso deve ser fornecido para as informações de conteúdo publicado associadas a esse conteúdo. O serviço de distribuição de mesmo nível usado para publicar o conteúdo pode fornecer as informações de conteúdo associadas. Depois que o consumidor tiver as informações de conteúdo, outras APIs de distribuição de mesmo nível poderão ser usadas para solicitar conteúdo do serviço de distribuição de mesmo nível. O serviço de distribuição de mesmo nível tentará recuperar o conteúdo da rede local. Se o conteúdo não estiver disponível, o aplicativo cliente será responsável por recuperar o conteúdo do servidor de origem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Remoção da publicação** | Para aplicativos que publicaram conteúdo no serviço de distribuição de mesmo nível, a função [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) foi fornecida para permitir que o conteúdo seja cancelado. Depois que o conteúdo tiver sido cancelado, o serviço de distribuição de pares local não fornecerá mais as informações de conteúdo associadas a esse conteúdo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Conclusões assíncronas

A API de distribuição de pares dá suporte a um modelo de API assíncrona e, como resultado, as APIs de distribuição de pares permitem o uso de portas ou eventos de conclusão de e/s como mecanismos de sinalização para processar conclusões de operação de distribuição de pares assíncronos. Para qualquer mecanismo, a distribuição de mesmo nível usa uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Em geral, a distribuição de pares usa a propriedade de uma estrutura **sobreposta** e quaisquer parâmetros de saída que o cliente passa para funções de API assíncronas. O cliente não deve acessar esses recursos até que a função assíncrona específica seja concluída. Assim que as funções assíncronas forem concluídas, o serviço de distribuição de mesmo nível não exigirá mais acesso a esses recursos e eles poderão ser reutilizados à medida que o aplicativo de chamada se ajustar.

Não haverá nenhuma conclusão assíncrona se a função retornar qualquer código de erro diferente de **\_ e/ \_ s de erro pendente**. O retorno de um valor diferente de **\_ e/ \_ s de erro** significa que a chamada falhou de forma síncrona. Se a API de distribuição de pares retornar **\_ e/s de erro \_ pendente**, o chamador deverá aguardar a conclusão assíncrona.

O código de erro da conclusão assíncrona pode ser recuperado de uma das duas maneiras:

**Conclusão com base na porta de conclusão de e/s**

O usuário invoca o mecanismo de porta de conclusão de e/s fornecendo um identificador de porta de conclusão e uma chave de conclusão para as seguintes funções de API:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

O usuário cria uma porta de conclusão chamando [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Esse identificador de porta de conclusão pode ser usado simultaneamente para outras operações de e/s assíncronas, bem como operações específicas de distribuição de pares.

O chamador deve usar a função [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para gerenciar a conclusão assíncrona. Se a operação assíncrona falhar, a função **GetQueuedCompletionStatus** retornará **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro apropriado. O chamador deve ignorar todos os campos da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) se o código de erro for algo diferente do **\_ êxito do erro**. A operação assíncrona terá sucesso se a função **GetQueuedCompletionStatus** retornar **true**.

Para obter mais informações [, consulte portas de conclusão de e/s](/windows/desktop/FileIO/i-o-completion-ports).

**Conclusão baseada em evento**

Se o chamador definir um identificador de evento válido para o campo *hEvent* da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , a distribuição de mesmo nível o usará para sinalizar que a operação de e/s assíncrona associada foi concluída.

Um chamador de thread pode gerenciar operações sobrepostas especificando um identificador para o objeto de evento de redefinição manual da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) em uma das funções de espera. Depois que o evento é sinalizado, o chamador deve chamar [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) passando na estrutura **sobreposta** apropriada. **PeerGetOverlappedResult** retornará **false** e o chamador deverá chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro. O chamador deve ignorar todos os campos da estrutura **sobreposta** se o código de erro for algo diferente do **\_ êxito do erro**. A operação assíncrona terá sucesso se a função **PeerGetOverlappedResult** retornar **true**.

Se o chamador fornecer uma porta de conclusão junto com um evento, o evento será usado como o mecanismo de conclusão.

**Windows 7:** Use a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) em vez de [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API de distribuição de pares](peer-distribution-api-reference.md)
</dt> </dl>

 

