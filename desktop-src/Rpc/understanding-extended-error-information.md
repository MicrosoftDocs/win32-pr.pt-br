---
title: Noções básicas sobre informações de erro estendidas
description: Informações de erro estendidas são uma matriz de registros, cada um indicando a passagem do código de erro por meio de uma camada específica no sistema ou aplicativo.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e003214198b06f04479ec4c1a8d23cb1acedafda49eefcf2880741416901323e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011054"
---
# <a name="understanding-extended-error-information"></a>Noções básicas sobre informações de erro estendidas

Informações de erro estendidas são uma matriz de registros, cada um indicando a passagem do código de erro por meio de uma camada específica no sistema ou aplicativo. Se ocorrer um erro em um computador C, como ele é chamado a partir da máquina B, que, por sua vez, é chamado do computador A, o tempo de execução do RPC no computador C gera um ou mais registros que descrevem o erro e os transmite para a máquina B. a máquina B pode adicionar um ou mais registros ao início da cadeia existente,  e passa a cadeia completa para um. Um pode adicionar um ou mais registros e exibir ou registrar as informações. Essencialmente, em seguida, a cadeia de erros estendidos representa o histórico do erro.

As informações de erro estendidas não substituem o código de erro (o \_ código de status RPC S \_ \* ). Independentemente de quanto ou se as informações de erro estendidas forem geradas, o código de erro permanecerá inalterado.

Cada registro de informações de erro estendido contém o seguinte. Consulte [**informações de \_ \_ erro \_ estendido RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) para obter mais informações:

-   ComputerName – este é o nome DNS não qualificado do computador no qual o erro foi originado. Somente os registros nos limites da máquina têm essas informações. Por exemplo, no cenário descrito anteriormente com as máquinas A, B e C, ComputerName é definido para os seguintes campos:

    | Record                            | Campo ComputerName |
    |-----------------------------------|--------------------|
    | Registro \# 1 gerado pela máquina C | \-                 |
    | Registro \# 2 gerado pela máquina C | \-                 |
    | Registro \# 3 gerado pela máquina C | C                  |
    | Registro \# 1 gerado pela máquina B | \-                 |
    | Registro \# 2 gerado pela máquina B | \-                 |
    | Registro \# 3 gerado pela máquina B | B                  |
    | Registro \# 1 gerado pela máquina A | \-                 |
    | Registro \# 2 gerado pela máquina A | \-                 |
    | Registro \# 3 gerado pelo computador A | \-                 |
    | Início da cadeia                 |                    |

    

     

<!-- -->

-   ProcessID — identificador de processo do processo que gerou o erro.
-   TimeStamp — hora em que o erro ocorreu, expresso em formato UTC.
-   Gerando componente – definição de código inteiro do componente lógico que gerou o erro. Os seguintes componentes estão definidos no momento:

    | Código | Nome              | Descrição                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Aplicativo       | O componente que possui a rotina de gerente para a chamada RPC específica                                                                                                                  |
    | 2    | Runtime           | O tempo de execução de RPC                                                                                                                                                                      |
    | 3    | Provedor de segurança | O provedor de segurança para esta chamada.                                                                                                                                                  |
    | 4    | NPFS              | O sistema de arquivos NPFS                                                                                                                                                                  |
    | 5    | RDR               | O redirecionador                                                                                                                                                                        |
    | 6    | NID               | O sistema de pipe nomeado. Isso pode ser NPFS ou RDR, mas em muitos casos o tempo de execução de RPC não sabe quem realizou a operação solicitada e, nesses casos, o NMP é retornado. |
    | 7    | IO                | O sistema de e/s ou um driver usado pelo sistema de e/s. Pode ser NPFS, RDR ou um provedor de Winsock.                                                                                 |
    | 8    | Winsock           | O provedor de Winsock                                                                                                                                                                  |
    | 9    | Código de Authz        | As APIs de autorização.                                                                                                                                                               |
    | 10   | LPC               | A instalação de chamada de procedimento local.                                                                                                                                                    |

    

     

<!-- -->

-   Status — código de erro gerado ou retornado pela camada
-   DetectionLocation — número exclusivo que identifica o local do código em que o erro foi detectado. Esse campo está vinculado ao código e será alterado de versão para versão. Uma lista separada dos locais de detecção encontrados com mais frequência será publicada.
-   Flags – sinalizadores que especificam informações sobre o registro. Os sinalizadores definidos no momento são EEInfoPreviousRecordsMissing e EEInfoNextRecordsMissing, correspondentes aos valores numéricos 1 e 2, respectivamente. Se EEInfoPreviousRecordsMissing for definido, um ou mais registros antes do registro ficarão ausentes. Se EEInfoNextRecordsMissing for definido, um ou mais registros depois desse registro estarão ausentes. Para obter uma descrição de por que os registros podem estar ausentes, consulte [confiabilidade das informações de erro estendidas](reliability-of-extended-error-information.md).
-   Até quatro parâmetros de erro. Um parâmetro de erro é uma estrutura de variante leve que fornece informações adicionais sobre o erro. As informações adicionais dependem do erro e do local de detecção. Os parâmetros podem ser do tipo LPSTR (cadeia de caracteres ANSI), Cadeia de caracteres Unicode (LPWSTR), valor longo (longo), valor curto (curto), ponteiro (Int64) ou nenhum.

 

 




