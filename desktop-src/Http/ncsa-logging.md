---
title: Registro em log do NCSA
description: O registro em log estendido do NCSA é um tipo de log do lado do servidor que pode ser habilitado em um grupo de URL.
ms.assetid: 14a2492a-3bcf-46f3-a3a5-1ea578516865
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5b9ef608da18264f4534c7e50e9672794a21bc61c91741feeb9e814c7afc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078306"
---
# <a name="ncsa-logging"></a>Registro em log do NCSA

O registro em log estendido do NCSA é um tipo de log do lado do servidor que pode ser habilitado em um grupo de URL. O formato de arquivo de log Comum ncSA é um formato fixo baseado em texto ASCII que não pode ser personalizado. O arquivo de log NCSA contém as ocorrências de cache de modo kernel da API do servidor HTTP. Esse tipo de registro em log pode ser habilitado somente em um grupo de URL; ele não pode ser usado na sessão do servidor.

O formato de arquivo de log Comum do NCSA registra os dados a seguir. Os dados na tabela estão na ordem de ocorrência no arquivo de log.



| Campo                                            | Descrição                                                                                                                                                                       |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Endereço do host remoto                              | Endereço IP do cliente que fez a solicitação.                                                                                                                               |
| Nome do log remoto                                  | Não usado. Esse valor é sempre um hífen.                                                                                                                                          |
| Nome do usuário                                        | O nome do usuário autenticado que acessou o servidor. Os usuários anônimos são indicados por um hífen. A melhor prática é que o aplicativo sempre forneça o nome de usuário. |
| Deslocamento de data, hora e horário de Greenwich (GMT) | A data e hora locais em que a atividade ocorreu. O deslocamento da hora média de Greenwich também é indicado.                                                                    |
| Versão de solicitação e protocolo                     | A versão do protocolo HTTP que o cliente usou.                                                                                                                                   |
| Código de status do serviço                              | O código de status HTTP. (Um valor de 200 indica que a solicitação foi concluída com êxito.)                                                                                         |
| Bytes sent                                       | O número de bytes enviados pelo servidor.                                                                                                                                           |



 

Nem todos os campos conterão informações. Para campos para os quais não há informações, um hífen (-) aparece como um espaço reservado. Se um campo contiver um caractere não impressível, a API do Servidor HTTP o substituirá por um sinal de a mais (+) para preservar o formato de arquivo de log. Isso normalmente ocorre com ataques de vírus, quando, por exemplo, um usuário mal-intencionado envia retornos de carro e feeds de linha que, se não são substituídos pelo sinal de mais (+), quebrariam o formato do arquivo de log. Os campos são separados por espaços e a hora é registrada como hora local com o deslocamento GMT.

O exemplo a seguir mostra uma entrada de arquivo de log Comum do NCSA, conforme exibido em um editor de texto.

``` syntax
172.21.13.45 - Microsoft\JohnDoe [07/Apr/2004:17:39:04 -0800] 
"GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0" 200 3401
```

O endereço IP do cliente é 172.21.13.45 e o nome de usuário é Microsoft \\ JohnDoe. O log foi registrado em 7 de abril de 2005 às 17:39:04 hora local com um deslocamento de Greenwich de 8 horas. O verbo de solicitação e a versão do protocolo eram "GET /scripts/iisadmin/ism.dll?http/serv HTTP/1.0". Os códigos de status foram 200 OK e o número de bytes enviados pelo cliente foi 3401.

 

 




