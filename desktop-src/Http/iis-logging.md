---
title: Log do IIS
description: O registro em log do IIS é um tipo de log do lado do servidor que pode ser habilitado em um grupo de URL.
ms.assetid: 2adfee73-090a-4bc1-827e-4b0e8075e2b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd92582e048a3b1a27d88f50f33c368345c72a836b72de9f2abb777bf5e9c59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102096"
---
# <a name="iis-logging"></a>Log do IIS

O registro em log do IIS é um tipo de log do lado do servidor que pode ser habilitado em um grupo de URL. O formato de arquivo de log do IIS é um formato fixo baseado em texto ASCII que não pode ser personalizado. O arquivo de log do IIS contém as ocorrências de cache do modo kernel da API do Servidor HTTP. Esse tipo de registro em log pode ser habilitado somente em um grupo de URL; ele não pode ser usado na sessão do servidor.

O formato de arquivo de log do IIS registra os dados a seguir. Os dados na tabela estão na ordem de ocorrência no arquivo de log.



| Campo                | Descrição                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Endereço IP do cliente    | Endereço IP do cliente que fez a solicitação.                                                                                                                               |
| Nome do usuário            | O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen. A melhor prática é que o aplicativo sempre forneça o nome de usuário. |
| Data                 | A data em que a atividade ocorreu.                                                                                                                                          |
| Tempo                 | A hora local em que a atividade ocorreu.                                                                                                                                    |
| Serviço e instância | O nome do serviço de Internet e o número da instância que estava em execução no cliente.                                                                                                     |
| Nome do servidor          | O nome do servidor no qual a entrada do arquivo de log foi gerada.                                                                                                                 |
| Endereço IP do servidor    | O endereço IP do servidor no qual a entrada do arquivo de log foi gerada.                                                                                                           |
| Tempo decorrido           | O período de tempo que a ação tomou em milissegundos.                                                                                                                         |
| Bytes de cliente enviados    | O número de bytes enviados pelo cliente.                                                                                                                                           |
| Bytes de servidor enviados    | O número de bytes enviados pelo servidor.                                                                                                                                           |
| Código de status do serviço  | Um valor de 200 indica que a solicitação foi atendida com êxito.                                                                                                             |
| Windows de status  | Um valor de 0 (zero) indica que a solicitação foi atendida com êxito.                                                                                                        |
| Tipo de solicitação         | O verbo de solicitação.                                                                                                                                                                 |
| Destino da operação  | O destino do verbo, por exemplo, Default.htm.                                                                                                                                 |
| Parâmetros           | Os parâmetros que são passados para um scrip.                                                                                                                                        |



 

Nem todos os campos conterão informações. Para campos para os quais não há informações, um hífen (-) aparece como um espaço reservado. Se um campo contiver um caractere não impressível, a API do Servidor HTTP o substituirá por um sinal de a mais (+) para preservar o formato de arquivo de log. Isso normalmente ocorre com ataques de vírus, quando, por exemplo, um usuário mal-intencionado envia retornos de carro e feeds de linha que, se não são substituídos pelo sinal de mais (+), quebrariam o formato do arquivo de log. Os campos são separados por vírgulas, tornando o formato mais fácil de ler do que os outros formatos ASCII, que usam espaços para separadores. A hora é registrada como hora local. O tempo necessário é registrado em milissegundos. Para obter mais informações sobre o campo de tempo de uso, consulte o tópico Registro em [log do W3C.](w3c-logging.md)

O exemplo a seguir mostra uma entrada de arquivo de log Comum do NCSA.

``` syntax
192.168.114.201, -, 03/20/05, 7:55:20, W3SVC2, SERVER, 
172.21.13.45, 4502, 163, 3223, 200, 0, GET, /DeptLogo.gif, -,
```

 

 




