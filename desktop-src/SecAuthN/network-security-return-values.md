---
description: Valores de retorno que um provedor de rede pode definir.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valores de retorno de segurança de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a362fde712d2a44565894aceb9d85172e488b53a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922316"
---
# <a name="network-security-return-values"></a>Valores de retorno de segurança de rede

Os valores de retorno que um provedor de rede pode definir incluem os seguintes códigos de erro.



| Códigos de erro         | Descrição                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sucesso no WN \_         | A função foi bem-sucedida.                                                                                                                                                                                                                                                                                                                 |
| \_não \_ há suporte para o WN  | Não há suporte para a função neste provedor de rede.                                                                                                                                                                                                                                                                                 |
| \_erro de rede WN \_      | Ocorreu um erro de rede desconhecido.                                                                                                                                                                                                                                                                                                       |
| \_mais \_ dados no WN      | O buffer de dados transmitido é insuficiente para conter todos os dados disponíveis.                                                                                                                                                                                                                                                         |
| \_ponteiro insatisfatório do WN \_    | Um ponteiro inválido foi especificado durante a chamada de função.                                                                                                                                                                                                                                                                     |
| \_valor inadequado de WN \_      | Um valor numérico inválido foi especificado durante a chamada de função.                                                                                                                                                                                                                                                               |
| \_senha inadequada do WN \_   | Uma senha incorreta foi especificada.                                                                                                                                                                                                                                                                                                    |
| acesso ao WN \_ \_ negado  | O chamador não tem permissões suficientes para concluir a operação.                                                                                                                                                                                                                                                              |
| \_função WN \_ ocupada  | Esta função não pode ser reinserida e está sendo usada no momento, ou o provedor ainda está sendo inicializado e ainda não está pronto para ser chamado. O provedor deve retornar esse código de erro somente se ele estiver disponível. Esse código de retorno é passado pelo MPR de volta para seu chamador e provavelmente fará com que o chamador tente novamente.<br/> |
| \_erro do Windows no WN \_  | Uma função necessária falhou.                                                                                                                                                                                                                                                                                                             |
| \_usuário inadequado do WN \_       | Um nome de usuário inválido foi especificado.                                                                                                                                                                                                                                                                                            |
| WN \_ fora \_ da \_ memória | Memória insuficiente para concluir a operação.                                                                                                                                                                                                                                                                                 |
| WN \_ não \_ conectado  | O dispositivo não é redirecionado.                                                                                                                                                                                                                                                                                                           |
| \_arquivos abertos do WN \_     | Não foi possível cancelar a conexão porque os arquivos ainda estão abertos.                                                                                                                                                                                                                                                                      |
| NetName do WN \_ inadequado \_    | O nome da rede não é válido.                                                                                                                                                                                                                                                                                                          |



 

 

 




