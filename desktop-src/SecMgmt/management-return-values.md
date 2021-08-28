---
description: Lista os valores retornados pelas funções de gerenciamento de segurança.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valores de retorno do Gerenciamento de Segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf20090ed4bbdfbeebb8fd77eafa8b9430df5aa816463ee32adb25116c7c3bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894249"
---
# <a name="security-management-return-values"></a>Valores de retorno do Gerenciamento de Segurança

Os valores de retorno de gerenciamento de segurança incluem o seguinte:

-   [Valores de retorno de anexo](#attachment-return-values)
-   [Valores de retorno da função de política LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valores de retorno de anexo

O conjunto de ferramentas configuração de segurança dá suporte aos seguintes códigos de retorno **SCESTATUS.** Esses valores são retornados pelas funções de suporte do anexo e essas funções implementadas ao escrever um mecanismo de anexo ou snap-in.



| Valor                            | Descrição                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ SUCCESS               | A função foi bem-sucedida.                                                                          |
| PARÂMETRO SCESTATUS \_ \_ INVÁLIDO    | Um dos parâmetros passados para a função não era válido.                                      |
| REGISTRO SCESTATUS \_ \_ NÃO \_ ENCONTRADO    | O registro especificado não foi encontrado no banco de dados de segurança.                                     |
| SCESTATUS \_ DADOS \_ INVÁLIDOS         | A função falhou porque alguns dados não são válidos.                                             |
| O OBJETO SCESTATUS \_ \_ EXISTE        | O objeto já existe.                                                                       |
| BUFFER SCESTATUS \_ \_ MUITO \_ PEQUENO    | O buffer passado para a função para receber dados não é grande o suficiente para receber todos os dados. |
| PERFIL SCESTATUS \_ \_ NÃO \_ ENCONTRADO   | O perfil especificado não foi encontrado.                                                             |
| SCESTATUS \_ FORMATO \_ RUIM           | O formato não é válido.                                                                         |
| RECURSO SCESTATUS \_ \_ NÃO É \_ SUFICIENTE | Não há memória suficiente.                                                                    |
| ACESSO SCESTATUS \_ \_ NEGADO        | O chamador não tem privilégios suficientes para concluir essa ação.                          |
| SCESTATUS \_ CANT \_ DELETE          | A função não pode excluir o item especificado.                                                   |
| ESTOURO DE \_ PREFIXO SCESTATUS \_      | Ocorreu um estouro de prefixo.                                                                      |
| SCESTATUS \_ OUTRO \_ ERRO          | Ocorreu um erro não especificado.                                                               |
| SCESTATUS \_ JÁ EM \_ EXECUÇÃO      | O serviço já está em execução.                                                                  |
| NÃO HÁ SUPORTE \_ PARA O SERVIÇO SCESTATUS \_ \_ | Não há suporte para o serviço especificado.                                                          |
| SCESTATUS \_ MOD \_ NÃO \_ ENCONTRADO       | Uma DLL do mecanismo de anexo listada no Registro não pode ser encontrada ou não pode ser carregada.      |
| EXCEÇÃO \_ SCESTATUS \_ NO \_ SERVIDOR | Ocorreu uma exceção no servidor.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valores de retorno da função de política LSA

A maioria das funções de política de LSA (Autoridade de Segurança [*Local)*](/windows/desktop/SecGloss/l-gly) retorna um valor NTSTATUS para indicar êxito ou falha. Os vários valores NTSTATUS são definidos em Ntstatus.h, que é distribuído com o DDK (Kit de Desenvolvimento de Driver) do Microsoft Windows.

Para converter um valor de retorno NTSTATUS em um Windows de erro, use a [**função LsaNtStatusToWinError.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)

A tabela a seguir lista os valores NTSTATUS que podem ser retornados por qualquer função LSA. (As seções de valor de retorno para algumas das funções LSA listam códigos de erro adicionais que a função pode retornar.) Esta tabela também lista o Windows código de erro que corresponde a cada valor NTSTATUS.



| Código NTSTATUS (Windows código de erro)                                        | Significado                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| STATUS \_ SUCCESS (ÊXITO \_ DO ERRO)<br/>                               | A função foi bem-sucedida.                                                                                                            |
| ACESSO \_ DE STATUS NEGADO \_ (ACESSO DE ERRO \_ \_ NEGADO)<br/>                 | O chamador não tem o acesso apropriado para concluir a operação.                                                                  |
| STATUS \_ INSUFICIENTE DE RECURSOS \_ (ERRO SEM RECURSOS DO \_ \_ \_ SISTEMA)<br/> | Não há recursos do sistema suficientes (como memória para alocar buffers) para concluir a chamada.                                        |
| STATUS \_ INTERNAL DB ERROR \_ \_ (ERRO INTERNO DO \_ \_ \_ BD)<br/>       | O banco de dados LSA contém uma inconsistência interna.                                                                                    |
| STATUS \_ INVALID \_ HANDLE (ERROR \_ INVALID \_ HANDLE)<br/>               | Indica que um objeto ou identificador RPC não é válido no [*contexto*](/windows/desktop/SecGloss/c-gly) usado.     |
| STATUS \_ ESTADO DO SERVIDOR INVÁLIDO \_ \_ (ERRO ESTADO DO SERVIDOR \_ \_ \_ INVÁLIDO)<br/> | Indica que o servidor LSA está desabilitado no momento.                                                                                         |
| PARÂMETRO \_ INVÁLIDO \_ STATUS (ERRO PARÂMETRO \_ \_ INVÁLIDO)<br/>         | Um dos parâmetros não é válido.                                                                                                     |
| STATUS \_ NENHUM PRIVILÉGIO DESSE TIPO \_ \_ \_ (ERRO NÃO É ESSE \_ \_ PRIVILÉGIO)<br/>       | Indica que um privilégio especificado não existe.                                                                                         |
| NOME DO OBJETO DE STATUS \_ \_ NÃO ENCONTRADO \_ \_ (ARQUIVO DE ERRO NÃO \_ \_ \_ ENCONTRADO)<br/>     | Um objeto no banco de dados de política LSA não foi encontrado. O objeto pode ter sido especificado por SID ou por nome, dependendo de seu tipo. |
| STATUS \_ MALSUCEDIDO (FALHA \_ DE GERAÇÃO DE \_ ERRO)<br/>                     | Falha genérica, como falha de conexão RPC.                                                                                        |



 

 

