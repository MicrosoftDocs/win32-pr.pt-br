---
description: Lista os valores retornados pelas funções de gerenciamento de segurança.
ms.assetid: ee55364e-8ffe-4a78-a49a-250756561770
title: Valores de retorno de gerenciamento de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2c67b79d03896960f7eb9a8631e1cd268284e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760008"
---
# <a name="security-management-return-values"></a>Valores de retorno de gerenciamento de segurança

Os valores de retorno do gerenciamento de segurança incluem o seguinte:

-   [Valores de retorno de anexo](#attachment-return-values)
-   [Valores de retorno da função de política LSA](#lsa-policy-function-return-values)

## <a name="attachment-return-values"></a>Valores de retorno de anexo

O conjunto de ferramentas de configuração de segurança oferece suporte aos seguintes códigos de retorno do **SCESTATUS** . Esses valores são retornados pelas funções de suporte de anexo e pelas funções implementadas ao gravar um mecanismo de anexo ou snap-in.



| Valor                            | Descrição                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------|
| SCESTATUS \_ êxito               | A função foi bem-sucedida.                                                                          |
| SCESTATUS \_ \_ parâmetro inválido    | Um dos parâmetros passados para a função não era válido.                                      |
| registro de SCESTATUS \_ \_ não \_ encontrado    | O registro especificado não foi encontrado no banco de dados de segurança.                                     |
| SCESTATUS \_ dados inválidos \_         | A função falhou porque alguns dados não eram válidos.                                             |
| o \_ objeto SCESTATUS \_ existe        | O objeto já existe.                                                                       |
| \_buffer SCESTATUS \_ muito \_ pequeno    | O buffer passado para a função para receber dados não é grande o suficiente para receber todos os dados. |
| \_perfil SCESTATUS \_ não \_ encontrado   | O perfil especificado não foi encontrado.                                                             |
| SCESTATUS \_ formato inadequado \_           | O formato não é válido.                                                                         |
| SCESTATUS \_ não \_ há \_ recursos suficientes | Memória insuficiente.                                                                    |
| \_acesso \_ negado ao SCESTATUS        | O chamador não tem privilégios suficientes para concluir esta ação.                          |
| SCESTATUS não \_ consegue \_ excluir          | A função não pode excluir o item especificado.                                                   |
| \_estouro de prefixo SCESTATUS \_      | Ocorreu um estouro de prefixo.                                                                      |
| SCESTATUS \_ outro \_ erro          | Ocorreu um erro não especificado.                                                               |
| SCESTATUS \_ já \_ está em execução      | O serviço já está em execução.                                                                  |
| \_ \_ não \_ há suporte para o serviço SCESTATUS | Não há suporte para o serviço especificado.                                                          |
| SCESTATUS \_ mod \_ não \_ encontrado       | Uma DLL do mecanismo de anexo listada no registro não pode ser encontrada ou não pode ser carregada.      |
| \_exceção SCESTATUS \_ no \_ servidor | Ocorreu uma exceção no servidor.                                                             |



 

## <a name="lsa-policy-function-return-values"></a>Valores de retorno da função de política LSA

A maioria das funções de política de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) retorna um valor NTSTATUS para indicar êxito ou falha. Os vários valores de NTSTATUS são definidos em Ntstatus. h, que é distribuído com o Microsoft Windows Driver Development Kit (DDK).

Para converter um valor de retorno de NTSTATUS em um código de erro do Windows, use a função [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) .

A tabela a seguir lista os valores de NTSTATUS que podem ser retornados por qualquer função de LSA. (As seções de valor de retorno para algumas das funções LSA listam códigos de erro adicionais que a função pode retornar.) Esta tabela também lista o código de erro do Windows que corresponde a cada valor de NTSTATUS.



| Código NTSTATUS (código de erro do Windows)                                        | Significado                                                                                                                                 |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| STATUS \_ êxito (êxito do erro \_ )<br/>                               | A função foi bem-sucedida.                                                                                                            |
| STATUS \_ \_ de acesso negado (erro de \_ acesso \_ negado)<br/>                 | O chamador não tem o acesso apropriado para concluir a operação.                                                                  |
| STATUS \_ de recursos insuficientes \_ (erro \_ sem \_ recursos do sistema \_ )<br/> | Não há recursos suficientes do sistema (como memória para alocar buffers) para concluir a chamada.                                        |
| \_erro interno \_ \_ do banco de status ( \_ erro interno do banco de erro \_ \_ )<br/>       | O banco de dados LSA contém uma inconsistência interna.                                                                                    |
| \_identificador inválido \_ do status ( \_ identificador inválido do erro \_ )<br/>               | Indica que um identificador de objeto ou RPC não é válido no [*contexto*](/windows/desktop/SecGloss/c-gly) usado.     |
| \_estado inválido \_ do servidor \_ de status (erro \_ inválido no \_ estado do servidor \_ )<br/> | Indica que o servidor LSA está desabilitado no momento.                                                                                         |
| \_parâmetro inválido \_ de status ( \_ parâmetro inválido de erro \_ )<br/>         | Um dos parâmetros não é válido.                                                                                                     |
| STATUS \_ sem \_ \_ privilégios (erro \_ sem \_ esse \_ privilégio)<br/>       | Indica que um privilégio especificado não existe.                                                                                         |
| \_ \_ nome do objeto \_ de status não \_ encontrado (arquivo de erro \_ \_ não \_ encontrado)<br/>     | Um objeto no banco de dados de política LSA não foi encontrado. O objeto pode ter sido especificado por SID ou por nome, dependendo de seu tipo. |
| STATUS \_ malsucedido (falha de Gen de erro \_ \_ )<br/>                     | Falha genérica, como falha de conexão RPC.                                                                                        |



 

 

