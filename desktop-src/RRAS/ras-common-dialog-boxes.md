---
title: Caixas de diálogo comuns de RAS
description: O Windows fornece um conjunto de funções que exibem as caixas de diálogo RAS fornecidas pelo sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3032da8b0647b48941d85fc4f085ddb8ced0125f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084840"
---
# <a name="ras-common-dialog-boxes"></a>Caixas de diálogo comuns de RAS

O Windows fornece um conjunto de funções que exibem as caixas de diálogo RAS fornecidas pelo sistema. Essas funções facilitam que os aplicativos exibam uma interface do usuário familiar para que os usuários possam executar tarefas de RAS. Por exemplo, os usuários podem estabelecer e monitorar conexões ou trabalhar com entradas de catálogo telefônico. No momento, o Windows 95 não oferece suporte a essas funções.

A função [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) exibe a caixa de diálogo principal **rede dial-up** . Nessa caixa de diálogo, o usuário pode discar, editar ou excluir uma entrada de catálogo telefônico selecionada, criar uma nova entrada de catálogo telefônico ou especificar preferências do usuário. A função **RasPhonebookDlg** usa a estrutura [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) para especificar parâmetros de entrada e saída adicionais. Por exemplo, você pode definir membros da estrutura para controlar a posição da caixa de diálogo na tela. Você pode usar a estrutura **RASPBDLG** para especificar uma função de retorno de chamada [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) que recebe notificações de atividade do usuário enquanto a caixa de diálogo está aberta. Por exemplo, o RAS chama sua função **RasPBDlgFunc** se o usuário disca, edita, cria ou exclui uma entrada de catálogo telefônico.

Você pode usar a função [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para iniciar uma operação de conexão RAS sem exibir a caixa de diálogo principal **rede dial-up** . Com o **RasDialDlg**, você especifica um número de telefone ou uma entrada de catálogo telefônico a ser chamada. A função exibe um fluxo de caixas de diálogo que indicam o estado da operação de conexão. A função **RasDialDlg** usa uma estrutura [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e a subentrada do catálogo telefônico a ser chamada.

Para exibir a folha de propriedades **rede dial-up** , chame a função [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) . Essa caixa de diálogo permite que o usuário monitore o status de conexões existentes. A função **RasMonitorDlg** usa uma estrutura [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e a página da folha de propriedades para exibir na parte superior.

Você pode chamar a função [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para exibir uma folha de propriedades para criar, editar ou copiar uma entrada de catálogo telefônico. A função **RasEntryDlg** usa uma estrutura [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e o tipo de operação de catálogo telefônico.

 

 