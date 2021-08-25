---
title: Caixas de diálogo comuns do RAS
description: Windows fornece um conjunto de funções que exibem as caixas de diálogo RAS fornecidas pelo sistema.
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be93db8e8d1819abe56d98bb293a7b6b027089be0648b00f7848d5204e911ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909716"
---
# <a name="ras-common-dialog-boxes"></a>Caixas de diálogo comuns do RAS

Windows fornece um conjunto de funções que exibem as caixas de diálogo RAS fornecidas pelo sistema. Essas funções facilitam a exibição de uma interface do usuário familiar para que os usuários possam executar tarefas RAS. Por exemplo, os usuários podem estabelecer e monitorar conexões ou trabalhar com entradas de lista telefônica. Windows 95 atualmente não dá suporte a essas funções.

A [**função RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) exibe a caixa de **Sistema de Rede de Conexão Discada** principal. Nessa caixa de diálogo, o usuário pode discar, editar ou excluir uma entrada de lista telefônica selecionada, criar uma nova entrada de agenda telefônica ou especificar preferências do usuário. A **função RasPhonebookDlg** usa a estrutura [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85)) para especificar parâmetros de entrada e saída adicionais. Por exemplo, você pode definir membros da estrutura para controlar a posição da caixa de diálogo na tela. Você pode usar a estrutura **RASPBDLG** para especificar uma função de retorno de chamada [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) que recebe notificações de atividade do usuário enquanto a caixa de diálogo está aberta. Por exemplo, RAS chama sua **função RasPBDlgFunc** se o usuário disca, edita, cria ou exclui uma entrada de livro telefônica.

Você pode usar a [**função RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) para iniciar uma operação de conexão RAS sem exibir a caixa **de Sistema de Rede de Conexão Discada** principal. Com **RasDialDlg**, você especifica um número de telefone ou uma entrada de lista telefônica para chamar. A função exibe um fluxo de caixas de diálogo que indicam o estado da operação de conexão. A **função RasDialDlg** usa uma estrutura [**RASDIALDLG**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e a subentrada de phone-book a ser chamada.

Para exibir a **Sistema de Rede de Conexão Discada** de propriedades, chame a [**função RasMonitorDlg.**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) Essa caixa de diálogo permite que o usuário monitore o status das conexões existentes. A **função RasMonitorDlg** usa uma estrutura [**RASMONITORDLG**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e a página da folha de propriedades a ser exibida na parte superior.

Você pode chamar a [**função RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) para exibir uma folha de propriedades para criar, editar ou copiar uma entrada de phone-book. A **função RasEntryDlg** usa uma estrutura [**RASENTRYDLG**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85)) para especificar parâmetros de entrada e saída adicionais, como a posição da caixa de diálogo e o tipo de operação de agenda telefônica.

 

 