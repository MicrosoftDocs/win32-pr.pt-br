---
title: Log do NCSA
description: O log estendido do NCSA é um tipo de registro no servidor que pode ser habilitado em um grupo de URLs.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04db62d5d561fb227f7a46a33c2aefcacd943b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637053"
---
# <a name="ncsa-logging"></a>Log do NCSA

O log estendido do NCSA é um tipo de registro no servidor que pode ser habilitado em um grupo de URLs. O formato do arquivo de log comum do NCSA é um formato baseado em texto ASCII fixo que não pode ser personalizado. O arquivo de log do NCSA contém as ocorrências de cache do modo kernel da API do servidor HTTP. Esse tipo de log só pode ser habilitado em um grupo de URLs; Ele não pode ser usado na sessão do servidor.

O formato do arquivo de log comum do NCSA registra os dados a seguir. Os dados na tabela estão na ordem de ocorrência no arquivo de log.



| Campo                                            | Descrição                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Endereço de host remoto                              | Endereço IP do cliente que fez a solicitação.                                                                                                                               |
| Nome do log remoto                                  | Não usado. Esse valor é sempre um hífen.                                                                                                                                          |
| Nome de usuário                                        | O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen. A prática recomendada é que o aplicativo sempre forneça o nome de usuário. |
| Deslocamento de data, hora e hora de Greenwich (GMT) | A data e a hora locais em que a atividade ocorreu. O deslocamento do tempo médio de Greenwich também é indicado.                                                                    |
| Versão de protocolo e solicitação                     | A versão do protocolo HTTP que o cliente usou.                                                                                                                                   |
| Código de status do serviço                              | O código de status HTTP. (Um valor de 200 indica que a solicitação foi concluída com êxito.)                                                                                         |
| Bytes sent                                       | O número de bytes enviados pelo servidor.                                                                                                                                           |



 

Nem todos os campos conterão informações. Para campos para os quais não há informações, um hífen (-) aparece como um espaço reservado. Se um campo contiver um caractere não imprimível, a API do servidor HTTP o substituirá por um sinal de adição (+) para preservar o formato do arquivo de log. Isso normalmente ocorre com ataques de vírus, quando, por exemplo, um usuário mal-intencionado envia retornos de carro e feeds de linha que, se não forem substituídos pelo sinal de adição (+), quebraria o formato do arquivo de log. Os campos são separados por espaços e a hora é registrada como hora local com o deslocamento GMT.

O exemplo a seguir mostra uma entrada de arquivo de log comum do NCSA, como exibido em um editor de texto.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

O endereço IP do cliente é 172.21.13.45 e o nome de usuário é Microsoft \\ davibarros. O log foi gravado em 7 de abril de 2005 às 17:39:04 hora local com um deslocamento de Greenwich de 8 horas. A versão de protocolo e o verbo de solicitação foram "GET/scripts/IISADMIN/ism.dll? http/serv HTTP/1.0". Os códigos de status eram 200 OK e o número de bytes enviados pelo cliente foi 3401.

 

 




