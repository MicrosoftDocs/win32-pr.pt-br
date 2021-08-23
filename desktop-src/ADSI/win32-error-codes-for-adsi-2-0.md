---
title: Códigos de erro do Win32 para ADSI 2.0
description: A tabela a seguir lista as mensagens de erro LDAP para ADSI 2.0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Códigos de erro do Win32 para ADSI 2.0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea81b4d277ad43cb2278d23549e370df1d11b3058be1e9c8b0f8b9329eabe26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589746"
---
# <a name="win32-error-codes-for-adsi-20"></a>Códigos de erro do Win32 para ADSI 2.0

A tabela a seguir lista as mensagens de erro LDAP para ADSI 2.0.



| Valor do erro ADSI | Mensagem LDAP                           | Mensagem Win32                        | Descrição                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP \_ SUCCESS**                      | **NENHUM \_ ERRO**                        | Êxito na operação.                                 |
| 0x80070002       | **LDAP \_ NÃO É UM OBJETO DESSE \_ \_ TIPO**             | **ARQUIVO \_ DE ERRO NÃO \_ \_ ENCONTRADO**          | O objeto não existe.                               |
| 0x80070005       | **NÃO HÁ SUPORTE PARA O MÉTODO LDAP \_ \_ \_ \_ AUTH** | **ACESSO \_ DE ERRO \_ NEGADO**            | Não há suporte para o método de autenticação.                 |
| 0x80070005       | **AUTH \_ FORTE \_ LDAP \_ NECESSÁRIA**       | **ACESSO \_ DE ERRO \_ NEGADO**            | Requer autenticação forte.                      |
| 0x80070005       | **\_AUTH LDAP \_ INADEQUADA**          | **ACESSO \_ DE ERRO \_ NEGADO**            | Autenticação inadequada.                        |
| 0x80070005       | **DIREITOS LDAP \_ \_ INSUFICIENTES**         | **ACESSO \_ DE ERRO \_ NEGADO**            | O usuário tem direitos de acesso insuficientes.                 |
| 0x80070005       | **LDAP \_ AUTH \_ UNKNOWN**                | **ACESSO \_ DE ERRO \_ NEGADO**            | Erro de autenticação desconhecido.               |
| 0x80070008       | **LDAP \_ SEM \_ MEMÓRIA**                   | **ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**       | O sistema está sem memória.                             |
| 0x8007001F       | **LDAP \_ OUTROS**                        | **FALHA \_ DE GERAÇÃO DE \_ ERRO**              | Ocorreu um erro desconhecido.                              |
| 0x8007001F       | **ERRO LOCAL DO \_ LDAP \_**                 | **FALHA \_ DE GERAÇÃO DE \_ ERRO**              | Ocorreu um erro local.                                |
| 0x80070037       | **LDAP \_ INDISPONÍVEL**                  | **O \_ DEV \_ DE ERRO NÃO \_ EXISTE**           | O servidor não está disponível.                             |
| 0x8007003A       | **LDAP \_ SERVER \_ DOWN**                 | **ERRO \_ \_ RESP DE NET \_ RUIM**            | Não é possível contatar o servidor LDAP.                      |
| 0x8007003B       | **ERRO DE CODIFICAÇÃO LDAP \_ \_**              | **ERRO \_ ERRO UNEXP \_ NET \_ ERR**           | Ocorreu um erro de codificação.                             |
| 0x8007003B       | **ERRO DE \_ DECODIFICAÇÃO DE LDAP \_**              | **ERRO \_ ERRO UNEXP \_ NET \_ ERR**           | Ocorreu um erro de decodificação.                             |
| 0x80070044       | **LIMITE DE ADMINISTRADOR \_ LDAP \_ \_ EXCEDIDO**       | **ERRO \_ MUITOS \_ \_ NOMES**          | Limite de administração excedido no servidor.         |
| 0x80070056       | **CREDENCIAIS \_ INVÁLIDAS DO LDAP \_**         | **ERRO \_ SENHA \_ INVÁLIDA**         | A credencial não é válida.                                |
| 0x80070057       | **SINTAXE \_ DN INVÁLIDA \_ DE LDAP \_**          | **ERRO \_ PARÂMETRO \_ INVÁLIDO**        | O nome diferenciado tem sintaxe que não é válida.     |
| 0x80070057       | **VIOLAÇÃO DE \_ NOMENUIDADE \_ LDAP**            | **ERRO \_ PARÂMETRO \_ INVÁLIDO**        | Violação de nomeação.                                    |
| 0x80070057       | **VIOLAÇÃO DA CLASSE DE OBJETO LDAP \_ \_ \_**     | **ERRO \_ PARÂMETRO \_ INVÁLIDO**        | Violação de classe de objeto.                              |
| 0x80070057       | **ERRO DE FILTRO LDAP \_ \_**                | **ERRO \_ PARÂMETRO \_ INVÁLIDO**        | O filtro de pesquisa é ruim.                                |
| 0x80070057       | **ERRO DE PARAM LDAP \_ \_**                 | **ERRO \_ PARÂMETRO \_ INVÁLIDO**        | O parâmetro ruim foi passado para uma rotina.               |
| 0X8007006E       | **ERRO DE OPERAÇÕES LDAP \_ \_**            | **FALHA \_ AO ABRIR \_ ERRO**              | Ocorreu um erro de operação.                            |
| 0x8007007A       | **RESULTADOS LDAP \_ \_ MUITO \_ GRANDES**          | **ERRO \_ BUFFER \_ INSUFICIENTE**      | O conjunto de resultados é muito grande.                            |
| 0x8007007B       | **sintaxe de LDAP \_ inválida \_**              | **\_nome inválido do erro \_**             | Sintaxe inválida.                                    |
| 0x8007007C       | **\_erro de protocolo LDAP \_**              | **ERRO \_ de \_ nível inválido**            | Erro de protocolo.                                      |
| 0x800700B7       | **o LDAP \_ já \_ existe**              | **o erro \_ já \_ existe**           | O objeto já existe.                               |
| 0x800700EA       | **\_resultados parciais LDAP \_**             | **ERRO de \_ mais \_ dados**                | Resultados parciais e referências recebidas.              |
| 0x800700EA       | **LDAP \_ ocupado**                         | **ERRO \_ ocupado**                      | O servidor está ocupado.                                      |
| 0x800703EB       | **LDAP não está sendo \_ \_ \_ executado**       | **ERRO \_ \_ não pode \_ ser concluído**        | O servidor não pode executar a operação.                     |
| 0x8007041D       | **\_tempo limite do LDAP**                      | **\_ \_ tempo limite de solicitação de serviço de erro \_** | A pesquisa atingiu o tempo limite.                                    |
| 0x800704B8       | **comparação de LDAP \_ \_ falso**               | **erro \_ estendido de erro \_**           | Comparação de **false** produzida.                           |
| 0x800704B8       | **comparação de LDAP \_ \_ true**                | **erro \_ estendido de erro \_**           | Comparação produzida como **verdadeira**.                            |
| 0x800704B8       | **referência de LDAP \_**                     | **erro \_ estendido de erro \_**           | Não é possível resolver a referência.                             |
| 0x800704B8       | **\_extensão crit não disponível de LDAP \_ \_** | **erro \_ estendido de erro \_**           | A extensão crítica não está disponível.                   |
| 0x800704B8       | **o LDAP \_ não tem \_ tal \_ atributo**          | **erro \_ estendido de erro \_**           | O atributo solicitado não existe.                  |
| 0x800704B8       | **tipo de LDAP \_ INdefinido \_**              | **erro \_ estendido de erro \_**           | O tipo não está definido.                                 |
| 0x800704B8       | **\_correspondência inadequada de LDAP \_**      | **erro \_ estendido de erro \_**           | Houve uma correspondência inadequada.                 |
| 0x800704B8       | **\_violação de restrição de LDAP \_**        | **erro \_ estendido de erro \_**           | Houve uma violação de restrição.                     |
| 0x800704B8       | **\_existe um atributo \_ ou \_ valor \_ LDAP** | **erro \_ estendido de erro \_**           | O atributo existe ou o valor foi atribuído. |
| 0x800704B8       | **\_problema de alias LDAP \_**               | **erro \_ estendido de erro \_**           | O alias não é válido.                                  |
| 0x800704B8       | **o LDAP \_ é \_ folha**                     | **erro \_ estendido de erro \_**           | O objeto é uma folha.                                    |
| 0x800704B8       | **\_problema de \_ DEREF do alias LDAP \_**        | **erro \_ estendido de erro \_**           | Não é possível desreferenciar o alias.                        |
| 0x800704B8       | **\_detecção de loop LDAP \_**                 | **erro \_ estendido de erro \_**           | O loop foi detectado.                                   |
| 0x800704B8       | **LDAP \_ não \_ permitido \_ em não \_ folha**    | **erro \_ estendido de erro \_**           | A operação não é permitida em um objeto não folha.       |
| 0x800704B8       | **LDAP \_ não \_ permitido \_ em \_ RDN**        | **erro \_ estendido de erro \_**           | A operação não é permitida em RDN.                     |
| 0x800704B8       | **LDAP \_ sem \_ classe de objeto \_ \_ mods**      | **erro \_ estendido de erro \_**           | Não é possível modificar a classe de objeto.                          |
| 0x800704B8       | **o LDAP \_ afeta \_ vários \_ DSAs**      | **erro \_ estendido de erro \_**           | Vários agentes de serviço de diretórios são afetados.      |
| 0x800704C7       | **\_usuário LDAP \_ cancelado**              | **ERRO \_ cancelado**                 | O usuário cancelou a operação.                     |
| 0x80070718       | **timelimite de LDAP \_ \_ excedido**          | **ERRO \_ sem \_ \_ cota suficiente**        | Limite de tempo excedido.                                 |
| 0x80070718       | **\_SIZELIMIT LDAP \_ excedido**          | **ERRO \_ sem \_ \_ cota suficiente**        | Limite de tamanho excedido.                                 |



 

No ADSI 2,0, várias mensagens de erro LDAP são mapeadas para um código de erro do Win32 como erro **\_ \_ estendido de erro**. Chame [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar a cadeia de caracteres de erro retornada pelo servidor. Para obter mais informações, consulte [mensagens de erro estendidas da ADSI](adsi-extended-error-messages.md) abaixo.

 

 




