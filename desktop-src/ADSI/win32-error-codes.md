---
title: Códigos de erro do Win32
description: A tabela a seguir lista as mensagens de erro LDAP para ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- ADSI de códigos de erro Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d8151c07fb6470d395f15e088ae5e50f3e43bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915876"
---
# <a name="win32-error-codes"></a>Códigos de erro do Win32

A tabela a seguir lista as mensagens de erro LDAP para ADSI.



| Valor de erro ADSI | Mensagem LDAP                           | Mensagem Win32                               | Descrição                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **êxito de LDAP \_**                      | **SEM \_ erros**                               | Operação bem-sucedida.                             |
| 0x80070005L      | **\_direitos insuficientes do LDAP \_**         | **ERRO de \_ acesso \_ negado**                   | O usuário tem direitos de acesso insuficientes.             |
| 0x80070008L      | **LDAP \_ sem \_ memória**                   | **ERRO \_ de \_ memória insuficiente \_**              | O sistema está sem memória.                         |
| 0x8007001fL      | **\_outro LDAP**                        | **\_falha de Gen de erro \_**                     | Erro desconhecido.                                   |
| 0x800700eaL      | **\_resultados parciais LDAP \_**             | **ERRO de \_ mais \_ dados**                       | Resultados parciais e referências recebidas.          |
| 0x800700eaL      | **LDAP \_ mais \_ resultados \_ a serem \_ retornados**    | **ERRO de \_ mais \_ dados**                       | Mais resultados devem ser retornados.                 |
| 0x800704c7L      | **\_usuário LDAP \_ cancelado**              | **ERRO \_ cancelado**                        | O usuário cancelou a operação.                     |
| 0x800704c9L      | **\_erro de conexão LDAP \_**               | **conexão de erro \_ \_ recusada**              | Não é possível estabelecer a conexão.                 |
| 0x8007052eL      | **\_credenciais inválidas do LDAP \_**         | **\_falha no logon do erro \_**                   | A credencial fornecida não é válida.                |
| 0x800705b4L      | **\_tempo limite do LDAP**                      | **\_tempo limite do erro**                          | A pesquisa atingiu o tempo limite.                                |
| 0x80071392L      | **o LDAP \_ já \_ existe**              | **o \_ objeto de erro \_ já \_ existe**          | O objeto já existe.                           |
| 0x8007200aL      | **o LDAP \_ não tem \_ tal \_ atributo**          | **ERRO \_ DS \_ sem \_ atributo \_ ou \_ valor**     | O atributo solicitado não existe.              |
| 0x8007200bL      | **sintaxe de LDAP \_ inválida \_**              | **ERRO \_ de \_ \_ sintaxe de atributo inválido DS \_**   | A sintaxe não é válida.                             |
| 0x8007200cL      | **tipo de LDAP \_ INdefinido \_**              | **ERRO \_ de \_ tipo de atributo DS \_ \_ indefinido**   | Tipo não definido.                                |
| 0x8007200dL      | **\_existe um atributo \_ ou \_ valor \_ LDAP** | **ERRO \_ o \_ atributo \_ ou o valor do DS \_ \_ existe** | O atributo existe ou o valor foi atribuído. |
| 0x8007200eL      | **LDAP \_ ocupado**                         | **ERRO \_ DS \_ ocupado**                         | O servidor está ocupado.                                  |
| 0x8007200fL      | **LDAP \_ não disponível**                  | **ERRO \_ DS \_ não disponível**                  | O servidor não está disponível.                         |
| 0x80072014L      | **\_violação de \_ classe de objeto LDAP \_**     | **ERRO \_ de \_ \_ violação de classe DS obj \_**        | Violação de classe de objeto.                          |
| 0x80072015L      | **LDAP \_ não \_ permitido \_ em não \_ folha**    | **ERRO \_ DS \_ \_ não consegue \_ em \_ folha**          | A operação não é permitida em um objeto não folha.  |
| 0x80072016L      | **LDAP \_ não \_ permitido \_ em \_ RDN**        | **ERRO \_ DS não \_ consegue \_ no \_ RDN**                | A operação não é permitida em um RDN.              |
| 0x80072017L      | **LDAP \_ sem \_ classe de objeto \_ \_ mods**      | **ERRO DS não é possível \_ \_ \_ \_ \_ classe obj**        | Não é possível modificar a classe de objeto.                      |
| 0x80072020L      | **\_erro de operações de LDAP \_**            | **erro \_ de \_ operações \_ DS**            | Ocorreu um erro de operação.                        |
| 0x80072021L      | **\_erro de protocolo LDAP \_**              | **erro \_ de \_ erro de protocolo DS \_**              | Ocorreu um erro de protocolo.                         |
| 0x80072022L      | **timelimite de LDAP \_ \_ excedido**          | **ERRO \_ de \_ limite de DS \_ excedido**          | Limite de tempo excedido.                             |
| 0x80072023L      | **\_SIZELIMIT LDAP \_ excedido**          | **ERRO \_ \_ SIZELIMIT DS \_ excedido**          | Limite de tamanho excedido.                             |
| 0x80072024L      | **limite de administrador de LDAP \_ \_ \_ excedido**       | **ERRO \_ de \_ limite de administrador DS \_ \_ excedido**       | Limite de administração excedido no servidor.     |
| 0x80072025L      | **comparação de LDAP \_ \_ falso**               | **ERRO \_ de \_ comparação de DS \_ falso**               | Comparação de **false** produzida.                       |
| 0x80072026L      | **comparação de LDAP \_ \_ true**                | **ERRO \_ de \_ comparação de DS \_ verdadeiro**                | Comparação produzida como **verdadeira**.                        |
| 0x80072027L      | **\_ \_ \_ não \_ há suporte para o método de autenticação LDAP** | **ERRO \_ \_ \_ \_ não \_ há suporte para o método de autenticação DS** | Não há suporte ao método de autenticação.      |
| 0x80072028L      | **\_autenticação forte de LDAP \_ \_ necessária**       | **ERRO \_ de \_ autenticação forte de DS \_ \_ necessária**       | A autenticação forte é necessária.               |
| 0x80072029L      | **\_autenticação inadequada de LDAP \_**          | **ERRO \_ de \_ autenticação inadequada de DS \_**          | A autenticação é inadequada.                 |
| 0x8007202aL      | **\_autenticação LDAP \_ desconhecida**                | **ERRO \_ de \_ autenticação DS \_ desconhecido**                | Ocorreu um erro de autenticação desconhecido.           |
| 0x8007202bL      | **referência de LDAP \_**                     | **ERRO \_ de \_ referência DS**                     | Não é possível resolver a referência.                         |
| 0x8007202cL      | **\_extensão crit não disponível de LDAP \_ \_** | **ERRO \_ de \_ extensão de crit não disponível DS \_ \_** | A extensão crítica não está disponível.               |
| 0x8007202dL      | **\_confidencialidade de LDAP \_ necessária**    | **ERRO \_ de \_ confidencialidade de DS \_ necessária**    | A confidencialidade é necessária.                     |
| 0x8007202eL      | **\_correspondência inadequada de LDAP \_**      | **ERRO \_ de \_ correspondência inadequada ao DS \_**      | Houve uma correspondência inadequada.             |
| 0x8007202fL      | **\_violação de restrição de LDAP \_**        | **ERRO \_ de \_ violação de restrição DS \_**        | Houve uma violação de restrição.                 |
| 0x80072030L      | **LDAP \_ não existe \_ tal \_ objeto**             | **ERRO \_ DS \_ não é \_ tal \_ objeto**             | O objeto não existe.                           |
| 0x80072031L      | **\_problema de alias LDAP \_**               | **ERRO \_ de \_ alias de DS \_**               | O alias não é válido.                              |
| 0x80072032L      | **\_sintaxe DN inválida do LDAP \_ \_**          | **ERRO \_ de \_ \_ sintaxe DN inválida DS \_**          | O nome diferenciado tem sintaxe inválida. |
| 0x80072033L      | **o LDAP \_ é \_ folha**                     | **ERRO \_ DS \_ é \_ folha**                     | O objeto é uma folha.                            |
| 0x80072034L      | **\_problema de \_ DEREF do alias LDAP \_**        | **ERRO \_ do \_ alias DS \_ DEREF \_ problema**        | Não é possível desreferenciar o alias.                    |
| 0x80072035L      | **LDAP não está sendo \_ \_ \_ executado**       | **ERRO \_ DS não \_ funcionado \_ para \_ executar**       | O servidor não pode executar a operação.                 |
| 0x80072036L      | **\_detecção de loop LDAP \_**                 | **ERRO \_ de \_ detecção de loop DS \_**                 | O loop foi detectado.                               |
| 0x80072037L      | **\_violação de nomenclatura de LDAP \_**            | **ERRO \_ de \_ violação de nomenclatura de DS \_**            | Houve uma violação de nomenclatura.                    |
| 0x80072038L      | **\_resultados LDAP \_ muito \_ grandes**          | **ERRO \_ de \_ objeto \_ DS \_ muito \_ grande**  | O conjunto de resultados é muito grande.                        |
| 0x80072039L      | **o LDAP \_ afeta \_ vários \_ DSAs**      | **ERRO o \_ DS \_ afeta \_ vários \_ DSAs**      | Vários agentes de serviço de diretórios são afetados.  |
| 0x8007203aL      | **\_servidor LDAP \_ inoperante**                 | **ERRO \_ de \_ servidor DS \_ inoperante**                 | Não é possível contatar o servidor LDAP.                  |
| 0x8007203bL      | **\_erro local de LDAP \_**                 | **erro \_ de \_ local \_ DS**                 | Ocorreu um erro local.                            |
| 0x8007203cL      | **\_erro de codificação LDAP \_**              | **erro \_ de \_ codificação \_ DS**              | Ocorreu um erro de codificação.                         |
| 0x8007203dL      | **\_erro de DEcodificação de LDAP \_**              | **erro \_ ao \_ decodificar \_ DS**              | Ocorreu um erro de decodificação.                         |
| 0x8007203eL      | **\_erro de filtro LDAP \_**                | **ERRO \_ de \_ filtro DS \_ desconhecido**              | O filtro de pesquisa é insatisfatório.                        |
| 0x8007203fL      | **\_erro de parâmetro LDAP \_**                 | **erro \_ de \_ erro de parâmetro DS \_**                 | Um parâmetro inadequado foi passado para uma função.        |
| 0x80072040L      | **LDAP \_ sem \_ suporte**               | **ERRO \_ DS \_ sem \_ suporte**               | Recurso sem suporte.                           |
| 0x80072041L      | **LDAP \_ nenhum \_ resultado \_ retornado**        | **ERRO \_ DS \_ nenhum \_ resultado \_ retornado**        | Os resultados não são retornados.                        |
| 0x80072042L      | **\_controle LDAP \_ não \_ encontrado**          | **ERRO \_ de \_ controle DS \_ não \_ encontrado**          | O controle não foi encontrado.                           |
| 0x80072043L      | **\_loop de cliente LDAP \_**                 | **ERRO \_ de \_ loop de cliente DS \_**                 | O loop do cliente foi detectado.                        |
| 0x80072044L      | **\_limite de referências LDAP \_ \_ excedido**    | **ERRO \_ \_ limite de referências DS \_ \_ excedido**    | Limite de referência excedido.                         |



 

 

 




