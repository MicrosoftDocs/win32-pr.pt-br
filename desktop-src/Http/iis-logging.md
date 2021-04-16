---
title: Log do IIS
description: O log do IIS é um tipo de registro no servidor que pode ser habilitado em um grupo de URLs.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d438d0926be2579fa526cc126c7f635a6eecd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750859"
---
# <a name="iis-logging"></a>Log do IIS

O log do IIS é um tipo de registro no servidor que pode ser habilitado em um grupo de URLs. O formato do arquivo de log do IIS é um formato baseado em texto ASCII fixo que não pode ser personalizado. O arquivo de log do IIS contém as ocorrências de cache do modo kernel da API do servidor HTTP. Esse tipo de log só pode ser habilitado em um grupo de URLs; Ele não pode ser usado na sessão do servidor.

O formato do arquivo de log do IIS registra os dados a seguir. Os dados na tabela estão na ordem de ocorrência no arquivo de log.



| Campo                | Descrição                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Endereço IP do cliente    | Endereço IP do cliente que fez a solicitação.                                                                                                                               |
| Nome de usuário            | O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen. A prática recomendada é que o aplicativo sempre forneça o nome de usuário. |
| Data                 | A data em que a atividade ocorreu.                                                                                                                                          |
| Hora                 | A hora local em que a atividade ocorreu.                                                                                                                                    |
| Serviço e instância | O nome do serviço de Internet e o número da instância que estava em execução no cliente.                                                                                                     |
| Nome do servidor          | O nome do servidor no qual a entrada do arquivo de log foi gerada.                                                                                                                 |
| Endereço IP do servidor    | O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.                                                                                                           |
| Tempo decorrido           | O período de tempo que a ação tomou em milissegundos.                                                                                                                         |
| Bytes de cliente enviados    | O número de bytes enviados pelo cliente.                                                                                                                                           |
| Bytes de servidor enviados    | O número de bytes enviados pelo servidor.                                                                                                                                           |
| Código de status do serviço  | Um valor de 200 indica que a solicitação foi atendida com êxito.                                                                                                             |
| Código de status do Windows  | Um valor de 0 (zero) indica que a solicitação foi atendida com êxito.                                                                                                        |
| Tipo de solicitação         | O verbo de solicitação.                                                                                                                                                                 |
| Destino da operação  | O destino do verbo, por exemplo, Default.htm.                                                                                                                                 |
| Parâmetros           | Os parâmetros que são passados para um cript.                                                                                                                                        |



 

Nem todos os campos conterão informações. Para campos para os quais não há informações, um hífen (-) aparece como um espaço reservado. Se um campo contiver um caractere não imprimível, a API do servidor HTTP o substituirá por um sinal de adição (+) para preservar o formato do arquivo de log. Isso normalmente ocorre com ataques de vírus, quando, por exemplo, um usuário mal-intencionado envia retornos de carro e feeds de linha que, se não forem substituídos pelo sinal de adição (+), quebraria o formato do arquivo de log. Os campos são separados por vírgulas, tornando o formato mais fácil de ler do que os outros formatos ASCII, que usam espaços para separadores. A hora é registrada como hora local. O tempo gasto é registrado em milissegundos. Para obter mais informações sobre o campo tempo gasto, consulte o tópico [log W3C](w3c-logging.md) .

O exemplo a seguir mostra uma entrada de arquivo de log comum do NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




