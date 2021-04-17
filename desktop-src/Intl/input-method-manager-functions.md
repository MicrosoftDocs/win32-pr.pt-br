---
description: Esta seção descreve as funções do IMM.
ms.assetid: 833c07eb-0ecf-41e2-9e01-8d83e51ffcef
title: Funções do Gerenciador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516a83e207434f5d8c2e073e770c878198bc98e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783288"
---
# <a name="input-method-manager-functions"></a>Funções do Gerenciador de métodos de entrada

Esta seção descreve as funções do IMM.



| Função                                                           | Descrição                                                                                                                |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**CreateIFECommonInstance**](/windows/desktop/api/msime/nf-msime-createifecommoninstance)         | Retorna um ponteiro para uma interface [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon) .                                                          |
| [**CreateIFEDictionaryInstance**](/windows/desktop/api/msime/nf-msime-createifedictionaryinstance) | Retorna um ponteiro para uma interface [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary) .                                                  |
| [**CreateIFELanguageInstance**](/windows/desktop/api/msime/nf-msime-createifelanguageinstance)     | Retorna um ponteiro para uma interface [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage) .                                                      |
| [**EnumInputContext**](/windows/desktop/api/Imm/nc-imm-imcenumproc)                       | Uma função de retorno de chamada definida pelo aplicativo que processa contextos de entrada fornecidos pela função **ImmEnumInputContext** .   |
| [**EnumRegisterWordProc**](/windows/desktop/api/Imm/nc-imm-registerwordenumproca)               | Uma função de retorno de chamada definida pelo aplicativo usada com a função **ImmEnumRegisterWord** .                                   |
| [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext)                 | Associa o contexto de entrada especificado à janela especificada.                                                          |
| [**ImmAssociateContextEx**](/windows/desktop/api/Imm/nf-imm-immassociatecontextex)             | Altera a associação entre o contexto do método de entrada e a janela especificada ou seus filhos.                         |
| [**ImmConfigureIME**](/windows/desktop/api/Imm/nf-imm-immconfigureimea)                         | Exibe a caixa de diálogo de configuração para o IME do identificador de localidade de entrada especificado.                                |
| [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext)                       | Cria um novo contexto de entrada, Alocando memória para o contexto e inicializando-o.                                        |
| [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)                     | Libera o contexto de entrada e libera a memória associada.                                                                    |
| [**ImmDisableIME**](/windows/desktop/api/Imm/nf-imm-immdisableime)                             | Desabilita o IME para um thread ou para todos os threads em um processo.                                                             |
| [**ImmDisableLegacyIME**](/windows/desktop/api/Imm/nf-imm-immdisablelegacyime)                 | Indica que esse thread é um thread de interface do usuário do aplicativo da Windows Store.                                                               |
| [**ImmDisableTextFrameService**](/windows/desktop/api/Imm/nf-imm-immdisabletextframeservice)   | Preterido. Desabilita o serviço de texto para o thread especificado.                                                            |
| [**ImmEnumInputContext**](/windows/desktop/api/Imm/nf-imm-immenuminputcontext)                 | Recupera o contexto de entrada para o thread especificado.                                                                      |
| [**ImmEnumRegisterWord**](/windows/desktop/api/Imm/nf-imm-immenumregisterworda)                 | Enumera as cadeias de caracteres de registro que têm a cadeia de leitura, o estilo e a cadeia de registro especificadas.                           |
| [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea)                                     | Acessa recursos de IMEs específicos que não estão disponíveis por meio de outras funções de API do IME.                           |
| [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)                 | Recupera uma lista de candidatos.                                                                                                |
| [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)       | Recupera o tamanho das listas de candidatos.                                                                                 |
| [**ImmGetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immgetcandidatewindow)             | Recupera informações sobre a janela de candidatos.                                                                         |
| [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)             | Recupera informações sobre a fonte lógica usada atualmente para exibir caracteres na janela de composição.               |
| [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)         | Recupera informações sobre a cadeia de caracteres de composição.                                                                        |
| [**ImmGetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immgetcompositionwindow)         | Recupera informações sobre a janela de composição.                                                                        |
| [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext)                             | Recupera o contexto de entrada associado à janela especificada.                                                          |
| [**ImmGetConversionList**](/windows/desktop/api/Imm/nf-imm-immgetconversionlista)               | Recupera a lista de resultados de conversão de caracteres ou palavras sem gerar nenhuma mensagem relacionada ao IME.                   |
| [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)           | Recupera o status de conversão atual.                                                                                   |
| [**ImmGetDefaultIMEWnd**](/windows/desktop/api/Imm/nf-imm-immgetdefaultimewnd)                 | Recupera o identificador de janela padrão para a classe IME.                                                                      |
| [**ImmGetDescription**](/windows/desktop/api/Imm/nf-imm-immgetdescriptiona)                     | Copia a descrição do IME para o buffer especificado.                                                                 |
| [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)                         | Recupera informações sobre erros.                                                                                        |
| [**ImmGetIMEFileName**](/windows/desktop/api/Imm/nf-imm-immgetimefilenamea)                     | Recupera o nome do arquivo do IME associado à localidade de entrada especificada.                                             |
| [**ImmGetImeMenuItems**](/windows/desktop/api/Imm/nf-imm-immgetimemenuitemsa)                   | Recupera os itens de menu que são registrados no menu IME de um contexto de entrada especificado.                                 |
| [**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)                       | Determina se o IME está aberto ou fechado.                                                                              |
| [**ImmGetProperty**](/windows/desktop/api/Imm/nf-imm-immgetproperty)                           | Recupera a propriedade e os recursos do IME associado à localidade de entrada especificada.                             |
| [**ImmGetRegisterWordStyle**](/windows/desktop/api/Imm/nf-imm-immgetregisterwordstylea)         | Recupera uma lista dos estilos com suporte pelo IME associado à localidade de entrada especificada.                            |
| [**ImmGetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immgetstatuswindowpos)             | Recupera a posição da janela de status.                                                                               |
| [**ImmGetVirtualKey**](/windows/desktop/api/Imm/nf-imm-immgetvirtualkey)                       | Recupera o valor da chave virtual original associado a uma mensagem de entrada de chave que o IME já processou.           |
| [**ImmInstallIME**](/windows/desktop/api/Imm/nf-imm-imminstallimea)                             | Instala um IME.                                                                                                           |
| [**ImmIsIME**](/windows/desktop/api/Imm/nf-imm-immisime)                                       | Determina se a localidade de entrada especificada tem um IME.                                                                       |
| [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)                           | Verifica as mensagens destinadas à janela do IME e envia essas mensagens para a janela especificada.                          |
| [**ImmNotifyIME**](/windows/desktop/api/Imm/nf-imm-immnotifyime)                               | Notifica o IME sobre as alterações no status do contexto de entrada.                                                         |
| [**ImmRegisterWord**](/windows/desktop/api/Imm/nf-imm-immregisterworda)                         | Registra uma cadeia de caracteres com o dicionário do IME associado à localidade de entrada especificada.                              |
| [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)                     | Libera o contexto de entrada e desbloqueia a memória associada no contexto de entrada.                                         |
| [**ImmRequestMessage**](/windows/desktop/api/Immdev/nf-immdev-immrequestmessagea)                     | Solicita uma mensagem do aplicativo.                                                                                   |
| [**ImmSetCandidateWindow**](/windows/desktop/api/Imm/nf-imm-immsetcandidatewindow)             | Define informações sobre a janela de candidatos.                                                                              |
| [**ImmSetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immsetcompositionfonta)             | Define a fonte lógica a ser usada para exibir os caracteres na janela de composição.                                              |
| [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa)         | Define os caracteres, atributos e cláusulas da composição e as cadeias de caracteres de leitura.                                       |
| [**ImmSetCompositionWindow**](/windows/desktop/api/Imm/nf-imm-immsetcompositionwindow)         | Define a posição da janela de composição.                                                                               |
| [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus)           | Define o status atual da conversão.                                                                                        |
| [**ImmSetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immsetopenstatus)                       | Abre ou fecha o IME.                                                                                                   |
| [**ImmSetStatusWindowPos**](/windows/desktop/api/Imm/nf-imm-immsetstatuswindowpos)             | Define a posição da janela de status.                                                                                    |
| [**ImmSimulateHotKey**](/windows/desktop/api/Imm/nf-imm-immsimulatehotkey)                     | Simula a tecla de acesso do IME especificada, causando a mesma resposta como se o usuário pressionasse a tecla de atalho na janela especificada. |
| [**ImmUnregisterWord**](/windows/desktop/api/Imm/nf-imm-immunregisterworda)                     | Remove uma cadeia de caracteres de registro do dicionário do IME associado à localidade de entrada especificada.                       |



 

 

 



