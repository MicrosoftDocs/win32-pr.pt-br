---
title: Códigos de erro do Win32
description: A tabela a seguir lista as mensagens de erro LDAP para ADSI.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- ADSI de códigos de erro Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d1986b0de2e4afeed0fccdcce62851acfaf104c3f360b7ea462410f4484f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118689886"
---
# <a name="win32-error-codes"></a>Códigos de erro do Win32

A tabela a seguir lista as mensagens de erro LDAP para ADSI.



| Valor de erro ADSI | Mensagem LDAP                           | Mensagem Win32                               | Descrição                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **êxito de LDAP \_**                      | **SEM \_ erros**                               | Êxito na operação.                             |
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
| 0x80072022L      | **LDAP \_ TIMELIMIT \_ EXCEDIDO**          | **ERRO \_ DS \_ TIMELIMIT \_ EXCEDIDO**          | Limite de tempo excedido.                             |
| 0x80072023L      | **LDAP \_ SIZELIMIT \_ EXCEDIDO**          | **ERRO \_ DS \_ SIZELIMIT \_ EXCEDIDO**          | Limite de tamanho excedido.                             |
| 0x80072024L      | **LIMITE DE ADMINISTRADOR \_ LDAP \_ \_ EXCEDIDO**       | **ERRO \_ LIMITE DE ADMINISTRADOR \_ \_ DS \_ EXCEDIDO**       | Limite de administração excedido no servidor.     |
| 0x80072025L      | **LDAP \_ COMPARE \_ FALSE**               | **ERRO \_ DS \_ COMPARE \_ FALSE**               | Compare FALSE yielded.                       |
| 0x80072026L      | **LDAP \_ COMPARE \_ TRUE**                | **ERRO \_ DS \_ COMPARE \_ TRUE**                | Compare TRUE yielded.                        |
| 0x80072027L      | **NÃO HÁ SUPORTE PARA O MÉTODO LDAP \_ \_ \_ \_ AUTH** | **ERRO NÃO HÁ SUPORTE PARA O MÉTODO \_ \_ DE AUTH \_ \_ \_ DS** | Não há suporte ao método de autenticação.      |
| 0x80072028L      | **AUTH \_ FORTE \_ LDAP \_ NECESSÁRIA**       | **ERRO \_ DS \_ \_ AUTH \_ FORTE NECESSÁRIA**       | A autenticação forte é necessária.               |
| 0x80072029L      | **\_AUTH LDAP \_ INADEQUADA**          | **ERRO \_ DS \_ \_ AUTH INADEQUADO**          | A autenticação é inadequada.                 |
| 0x8007202aL      | **LDAP \_ AUTH \_ UNKNOWN**                | **ERRO \_ DS \_ AUTH \_ UNKNOWN**                | Erro de autenticação desconhecido.           |
| 0x8007202bL      | **LDAP \_ REFERRAL**                     | **INDICAÇÃO \_ DE ERRO DS \_**                     | Não é possível resolver a indicação.                         |
| 0x8007202cL      | **EXTENSÃO CRIT LDAP \_ \_ \_ INDISPONÍVEL** | **ERRO \_ DS \_ EXTENSÃO \_ CRIT \_ INDISPONÍVEL** | A extensão crítica não está disponível.               |
| 0x8007202dL      | **CONFIDENCIALIDADE LDAP \_ \_ NECESSÁRIA**    | **ERRO \_ DS \_ \_ CONFIDENCIALIDADE NECESSÁRIA**    | A confidencialidade é necessária.                     |
| 0x8007202eL      | **CORRESPONDÊNCIA INADEQUADA DE LDAP \_ \_**      | **ERRO \_ DS \_ CORRESPONDÊNCIA \_ INADEQUADA**      | Houve uma correspondência inadequada.             |
| 0x8007202fL      | **VIOLAÇÃO DE \_ RESTRIÇÃO LDAP \_**        | **VIOLAÇÃO \_ DE RESTRIÇÃO DE ERRO \_ \_ DS**        | Houve uma violação de restrição.                 |
| 0x80072030L      | **LDAP \_ NÃO É UM OBJETO DESSE \_ \_ TIPO**             | **ERRO \_ DS \_ NENHUM OBJETO \_ DESSE \_ TIPO**             | O objeto não existe.                           |
| 0x80072031L      | **PROBLEMA DE ALIAS LDAP \_ \_**               | **ERRO \_ PROBLEMA DE ALIAS DS \_ \_**               | O alias não é válido.                              |
| 0x80072032L      | **SINTAXE \_ DN INVÁLIDA \_ DE LDAP \_**          | **ERRO \_ DS \_ SINTAXE \_ DN \_ INVÁLIDA**          | O nome diferenciado tem sintaxe que não é válida. |
| 0x80072033L      | **LDAP \_ É \_ FOLHA**                     | **O \_ ERRO DS \_ É \_ FOLHA**                     | O objeto é uma folha.                            |
| 0x80072034L      | **PROBLEMA DE \_ DEREF DO ALIAS \_ LDAP \_**        | **ERRO \_ PROBLEMA DE \_ DEREF DO ALIAS \_ DS \_**        | Não é possível desreferenciar o alias.                    |
| 0x80072035L      | **LDAP \_ \_ DESEMPESO PARA \_ EXECUTAR**       | **ERRO \_ DS \_ NÃO É PRECISO \_ \_ EXECUTAR**       | O servidor não pode executar a operação.                 |
| 0x80072036L      | **LDAP \_ LOOP \_ DETECT**                 | **ERRO \_ DE DETECÇÃO DE LOOP DS \_ \_**                 | Loop detectado.                               |
| 0x80072037L      | **VIOLAÇÃO DE \_ NOMENUIDADE \_ LDAP**            | **VIOLAÇÃO \_ DE \_ NOMEAÇÃO DE ERRO DS \_**            | Houve uma violação de nomeação.                    |
| 0x80072038L      | **RESULTADOS LDAP \_ \_ MUITO \_ GRANDES**          | **ERRO \_ OS RESULTADOS DO OBJETO DS SÃO MUITO \_ \_ \_ \_ GRANDES**  | O conjunto de resultados é muito grande.                        |
| 0x80072039L      | **LDAP \_ AFETA \_ VÁRIAS \_ DSAS**      | **O \_ ERRO DS \_ AFETA VÁRIAS \_ \_ DSAS**      | Vários agentes de serviço de diretórios são afetados.  |
| 0x8007203aL      | **LDAP \_ SERVER \_ DOWN**                 | **ERRO \_ DO SERVIDOR DS \_ \_ INOBADO**                 | Não é possível contatar o servidor LDAP.                  |
| 0x8007203bL      | **ERRO LOCAL DO \_ LDAP \_**                 | **ERRO \_ ERRO DS \_ LOCAL \_**                 | Ocorreu um erro local.                            |
| 0x8007203cL      | **ERRO DE CODIFICAÇÃO LDAP \_ \_**              | **ERRO \_ DE \_ CODIFICAÇÃO DS \_**              | Ocorreu um erro de codificação.                         |
| 0x8007203dL      | **ERRO DE \_ DECODIFICAÇÃO DE LDAP \_**              | **ERRO \_ DE \_ DECODIFICAÇÃO DE DS \_**              | Ocorreu um erro de decodificação.                         |
| 0x8007203eL      | **ERRO DE FILTRO LDAP \_ \_**                | **ERRO \_ FILTRO DS \_ \_ DESCONHECIDO**              | O filtro de pesquisa é ruim.                        |
| 0x8007203fL      | **ERRO DE PARAM LDAP \_ \_**                 | **ERRO \_ ERRO DE \_ PARAM DS \_**                 | Um parâmetro ruim foi passado para uma função.        |
| 0x80072040L      | **LDAP \_ SEM \_ SUPORTE**               | **ERRO \_ NÃO HÁ SUPORTE PARA \_ \_ DS**               | Recurso sem suporte.                           |
| 0x80072041L      | **LDAP \_ SEM \_ RESULTADOS \_ RETORNADOS**        | **ERRO \_ DS \_ NENHUM RESULTADO \_ \_ RETORNADO**        | Os resultados não são retornados.                        |
| 0x80072042L      | **CONTROLE LDAP \_ \_ NÃO \_ ENCONTRADO**          | **ERRO \_ CONTROLE DS \_ NÃO \_ \_ ENCONTRADO**          | O controle não foi encontrado.                           |
| 0x80072043L      | **LOOP DE CLIENTE LDAP \_ \_**                 | **LOOP \_ DE CLIENTE ERROR DS \_ \_**                 | O loop do cliente foi detectado.                        |
| 0x80072044L      | **LIMITE DE INDICAÇÃO LDAP \_ \_ \_ EXCEDIDO**    | **LIMITE \_ DE INDICAÇÃO DE ERRO DS \_ \_ \_ EXCEDIDO**    | Limite de indicação excedido.                         |



 

 

 




