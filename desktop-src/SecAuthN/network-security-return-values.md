---
description: Retornar valores que um provedor de rede pode definir.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valores de retorno de segurança de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40fd8e6e21d9e7671c1e7b9c3d008978628e28cb0fcb01c3df56359144e72e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921295"
---
# <a name="network-security-return-values"></a>Valores de retorno de segurança de rede

Os valores de retorno que um provedor de rede pode definir incluem os seguintes códigos de erro.



| Códigos de erro         | Description                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ SUCCESS         | A função foi bem-sucedida.                                                                                                                                                                                                                                                                                                                 |
| NÃO \_ HÁ \_ SUPORTE PARA WN  | Não há suporte para a função neste provedor de rede.                                                                                                                                                                                                                                                                                 |
| WN \_ NET \_ ERROR      | Ocorreu um erro de rede desconhecido.                                                                                                                                                                                                                                                                                                       |
| WN \_ MORE \_ DATA      | O buffer de dados passado é insuficiente para conter todos os dados disponíveis.                                                                                                                                                                                                                                                         |
| PONTEIRO RUIM DE \_ \_ WN    | Um ponteiro que não é válido foi especificado durante a chamada de função.                                                                                                                                                                                                                                                                     |
| VALOR RUIM DE WN \_ \_      | Um valor numérico que não é válido foi especificado durante a chamada de função.                                                                                                                                                                                                                                                               |
| WN \_ BAD \_ PASSWORD   | Uma senha incorreta foi especificada.                                                                                                                                                                                                                                                                                                    |
| ACESSO AO WN \_ \_ NEGADO  | O chamador não tem permissões suficientes para concluir a operação.                                                                                                                                                                                                                                                              |
| FUNÇÃO WN \_ \_ OCUPADO  | Essa função não pode ser reinserido e está sendo usada no momento ou o provedor ainda está inicializando e ainda não está pronto para ser chamado. O provedor só deverá retornar esse código de erro se ele estiver disponível. Esse código de retorno é passado pela MPR de volta para seu chamador e provavelmente faz com que o chamador volte a tentar.<br/> |
| WN \_ WINDOWS \_ ERROR  | Falha em uma função necessária.                                                                                                                                                                                                                                                                                                             |
| WN \_ BAD \_ USER       | Um nome de usuário que não é válido foi especificado.                                                                                                                                                                                                                                                                                            |
| WN \_ SEM \_ \_ MEMÓRIA | Não há memória suficiente para concluir a operação.                                                                                                                                                                                                                                                                                 |
| WN \_ NÃO \_ CONECTADO  | O dispositivo não é redirecionado.                                                                                                                                                                                                                                                                                                           |
| WN \_ OPEN \_ FILES     | Não foi possível cancelar a conexão porque os arquivos ainda estão abertos.                                                                                                                                                                                                                                                                      |
| WN \_ BAD \_ NETNAME    | O nome da rede não é válido.                                                                                                                                                                                                                                                                                                          |



 

 

 




