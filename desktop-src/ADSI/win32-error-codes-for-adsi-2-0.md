---
title: Códigos de erro do Win32 para ADSI 2,0
description: A tabela a seguir lista as mensagens de erro LDAP para o ADSI 2,0.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Códigos de erro do Win32 para ADSI do ADSI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e079fa6a98df28625f6307f774ce194712a52a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822173"
---
# <a name="win32-error-codes-for-adsi-20"></a>Códigos de erro do Win32 para ADSI 2,0

A tabela a seguir lista as mensagens de erro LDAP para o ADSI 2,0.



| Valor de erro ADSI | Mensagem LDAP                           | Mensagem Win32                        | Descrição                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **êxito de LDAP \_**                      | **SEM \_ erros**                        | Operação bem-sucedida.                                 |
| 0x80070002       | **LDAP \_ não existe \_ tal \_ objeto**             | **arquivo de erro \_ \_ não \_ encontrado**          | O objeto não existe.                               |
| 0x80070005       | **\_ \_ \_ não \_ há suporte para o método de autenticação LDAP** | **ERRO de \_ acesso \_ negado**            | Método de autenticação sem suporte.                 |
| 0x80070005       | **\_autenticação forte de LDAP \_ \_ necessária**       | **ERRO de \_ acesso \_ negado**            | Requer autenticação forte.                      |
| 0x80070005       | **\_autenticação inadequada de LDAP \_**          | **ERRO de \_ acesso \_ negado**            | Autenticação inadequada.                        |
| 0x80070005       | **\_direitos insuficientes do LDAP \_**         | **ERRO de \_ acesso \_ negado**            | O usuário tem direitos de acesso insuficientes.                 |
| 0x80070005       | **\_autenticação LDAP \_ desconhecida**                | **ERRO de \_ acesso \_ negado**            | Ocorreu um erro de autenticação desconhecido.               |
| 0x80070008       | **LDAP \_ sem \_ memória**                   | **ERRO \_ de \_ memória insuficiente \_**       | O sistema está sem memória.                             |
| 0x8007001F       | **\_outro LDAP**                        | **\_falha de Gen de erro \_**              | Ocorreu um erro desconhecido.                              |
| 0x8007001F       | **\_erro local de LDAP \_**                 | **\_falha de Gen de erro \_**              | Ocorreu um erro local.                                |
| 0x80070037       | **LDAP \_ não disponível**                  | **\_desenvolvimento de \_ erro \_ inexistente**           | O servidor não está disponível.                             |
| 0x8007003A       | **\_servidor LDAP \_ inoperante**                 | **ERRO \_ \_ resp net inadequado \_**            | Não é possível contatar o servidor LDAP.                      |
| 0x8007003B       | **\_erro de codificação LDAP \_**              | **ERRO \_ UNEXP \_ net \_ Err**           | Ocorreu um erro de codificação.                             |
| 0x8007003B       | **\_erro de DEcodificação de LDAP \_**              | **ERRO \_ UNEXP \_ net \_ Err**           | Ocorreu um erro de decodificação.                             |
| 0x80070044       | **limite de administrador de LDAP \_ \_ \_ excedido**       | **ERRO \_ em \_ muitos \_ nomes**          | Limite de administração excedido no servidor.         |
| 0x80070056       | **\_credenciais inválidas do LDAP \_**         | **\_senha inválida do erro \_**         | Credencial inválida.                                |
| 0x80070057       | **\_sintaxe DN inválida do LDAP \_ \_**          | **\_parâmetro inválido de erro \_**        | O nome diferenciado tem sintaxe inválida.     |
| 0x80070057       | **\_violação de nomenclatura de LDAP \_**            | **\_parâmetro inválido de erro \_**        | Violação de nomenclatura.                                    |
| 0x80070057       | **\_violação de \_ classe de objeto LDAP \_**     | **\_parâmetro inválido de erro \_**        | Violação de classe de objeto.                              |
| 0x80070057       | **\_erro de filtro LDAP \_**                | **\_parâmetro inválido de erro \_**        | O filtro de pesquisa é insatisfatório.                                |
| 0x80070057       | **\_erro de parâmetro LDAP \_**                 | **\_parâmetro inválido de erro \_**        | Parâmetro inadequado foi passado para uma rotina.               |
| 0X8007006E       | **\_erro de operações de LDAP \_**            | **\_ \_ falha ao abrir erro**              | Ocorreu um erro de operação.                            |
| 0x8007007A       | **\_resultados LDAP \_ muito \_ grandes**          | **ERRO \_ de \_ buffer insuficiente**      | O conjunto de resultados é muito grande.                            |
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

 

 




