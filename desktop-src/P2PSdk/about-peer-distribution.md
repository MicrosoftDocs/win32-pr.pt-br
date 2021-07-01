---
description: A API de Distribuição par, que dá suporte ao recurso Cache de Branch no Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, oferece um conjunto de APIs de plataforma que podem aumentar a capacidade de resposta de rede de aplicativos centralizados quando acessados de escritórios remotos e ajudar a reduzir a utilização geral da WAN (rede de longa distância) sem interferir nas tecnologias de segurança de rede.
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Sobre a distribuição de pares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c996aed35ac691284ba61b757d6ff5a88033aad
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120431"
---
# <a name="about-peer-distribution"></a>Sobre a distribuição de pares

A API de Distribuição par, que dá suporte ao recurso Cache de Branch no Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, oferece um conjunto de APIs de plataforma que podem aumentar a capacidade de resposta de rede de aplicativos centralizados quando acessados de escritórios remotos e ajudar a reduzir a utilização geral da WAN (rede de longa distância) sem interferir nas tecnologias de segurança de rede.

O sistema de Distribuição de Pares oferece um conjunto de APIs de plataforma utilizadas pelos editores que fornecem conteúdo digital e consumidores que o solicitam. Para diferenciar facilmente essas funções, pode ser mais fácil pensar no publicador em uma função de servidor e no consumidor em uma função de cliente. Além disso, é importante lembrar que, além dessas funções conceituais, o serviço distribuição de pares é um sistema par verdadeiro, conforme indicado pela capacidade de qualquer nó de Distribuição de Pares publicar e consumir conteúdo digital. As APIs da plataforma distribuição de pares são expostas a editores e consumidores por uma biblioteca de importação do Win32 (**PeerDist.Lib**).

O ciclo de vida do conteúdo fornecido por um editor e recuperado por um consumidor com o serviço distribuição de pares é composto pelas seguintes operações:



|                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Publicação de conteúdo** | A publicação é feita para produzir uma descrição do conteúdo com o termo Informações de **Conteúdo** ou Informações **de Conteúdo** para resumir. Essas Informações de Conteúdo podem ser usadas por uma instância do serviço distribuição de pares para autenticar e recriar o conteúdo. Quando o conteúdo é publicado por um aplicativo no serviço distribuição de pares, que é conceitualmente uma operação do lado do servidor, esse conteúdo se torna associado à Identidade do Publicador, que se baseia no SID do usuário associado ao token de acesso de thread. Essa associação é feita para limitar o acesso ao conteúdo por entidades não autorizadas. No entanto, é importante observar que o acesso às informações de conteúdo é equivalente ao acesso ao próprio conteúdo, pois as informações de conteúdo podem ser usadas para obter o conteúdo de pares ou de um cache hospedado.<br/> Há uma nova versão da estrutura de dados de informações de conteúdo no Windows 8; no entanto, a versão anterior ainda tem suporte. Para interoperar com clientes do Windows 7, um administrador pode configurar o serviço distribuição de pares para usar a versão anterior da estrutura de dados de informações de conteúdo.<br/> |
| **Recuperação de conteúdo**   | Para que um consumidor recupere conteúdo do serviço distribuição de pares, o acesso deve ser fornecido às Informações de Conteúdo publicadas associadas a esse conteúdo. O serviço distribuição de pares usado para publicar o conteúdo pode fornecer as Informações de Conteúdo associadas. Depois que o consumidor tiver as Informações de Conteúdo, outras APIs de Distribuição de Pares poderão ser usadas para solicitar conteúdo do serviço distribuição de pares. O serviço distribuição de pares tentará recuperar o conteúdo da rede local. Se o conteúdo não estiver disponível, o aplicativo cliente será responsável por recuperar o conteúdo do servidor de origem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Remoção de publicação** | Para aplicativos que publicaram conteúdo no serviço distribuição de pares, a função [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) foi fornecida para permitir que o conteúdo seja não publicado. Depois que o conteúdo tiver sido publicado, o serviço de Distribuição de Pares local não fornecerá mais as informações de conteúdo associadas a esse conteúdo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Preenchimentos assíncronos

A API de Distribuição de Pares dá suporte a um modelo de API assíncrona e, como resultado, as APIs de Distribuição Par permitem o uso de Portas de Conclusão de E/S ou Eventos como mecanismos de sinalização para processamento de preenchimentos de operação de distribuição par assíncrona. Para qualquer mecanismo, a Distribuição de Pares usa uma [**estrutura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Em geral, a Distribuição de Pares assume a propriedade de uma estrutura **OVERLAPPED** e todos os parâmetros que o Cliente passa para funções de API assíncronas. O Cliente não deve acessar esses recursos até que a função assíncrona específica seja concluída. Assim que as funções assíncronas são concluídas, o serviço distribuição de pares não exigirá mais acesso a esses recursos e eles poderão ser reutilizados conforme o aplicativo de chamada for adequado.

Não haverá nenhuma conclusão assíncrona se a função retornar qualquer código de erro diferente de **ERROR \_ IO \_ PENDING.** O retorno de um valor diferente de **ERROR \_ E/S \_ PENDING** significa que a chamada falhou de forma síncrona. Se a API de Distribuição de Pares retornar **ERRO \_ DE \_ E/S PENDENTE,** o chamador deverá aguardar a conclusão assíncrona.

O código de erro da conclusão assíncrona pode ser recuperado de uma das duas maneiras:

**Preenchimento baseado em porta de conclusão de E/S**

O usuário invoca o mecanismo de porta de conclusão de E/S fornecendo uma alça de porta de conclusão e uma chave de conclusão para as seguintes funções de API:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

O usuário cria uma porta de conclusão chamando [**CreateIoCompletionPort.**](/windows/desktop/FileIO/createiocompletionport) Esse alça de porta de conclusão pode ser usado simultaneamente para outras operações de E/S assíncronas, bem como operações específicas de Distribuição de Pares.

O chamador deve usar [**a função GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para gerenciar a conclusão assíncrona. Se a operação assíncrona falhar, a função **GetQueuedCompletionStatus** retornará **FALSE** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro apropriado. O chamador deverá ignorar todos os campos da estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) se o código de erro for diferente de **ERROR \_ SUCCESS.** A operação assíncrona terá êxito se a **função GetQueuedCompletionStatus** retornar **TRUE.**

Para obter mais informações, consulte [Portas de conclusão de E/S](/windows/desktop/FileIO/i-o-completion-ports).

**Conclusão baseada em evento**

Se o chamador define um alça de evento válido para o campo *hEvent* da estrutura [**OVERLAPPED,**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) a Distribuição de Pares o usará para sinalizar que a operação de E/S assíncrona associada foi concluída.

Um chamador de thread pode gerenciar operações sobreposição especificando um identificador para o objeto de evento de redefinição manual da estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) em uma das funções de espera. Depois que o Evento for sinalizado, o chamador deverá chamar [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) passando a estrutura **OVERLAPPED** apropriada. **PeerGetOverlappedResult** retornará **FALSE** e o chamador deverá chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o código de erro. O chamador deverá ignorar todos os campos da estrutura **OVERLAPPED** se o código de erro for diferente de **ERROR \_ SUCCESS.** A operação assíncrona terá êxito se a **função PeerGetOverlappedResult** retornar **TRUE.**

Se o chamador fornece uma porta de conclusão juntamente com um evento, o evento será usado como o mecanismo de conclusão.

**Windows 7:** Use a [**função GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) em vez de [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência da API de Distribuição de Pares](peer-distribution-api-reference.md)
</dt> </dl>

 

