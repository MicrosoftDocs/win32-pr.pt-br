---
description: A participação de um gravador em uma operação de backup ou restauração, e quais dos seus dados são salvos, depende de quais dos seus componentes são incluídos explicitamente como parte do documento de componentes de backup de um solicitante e da relação entre esses componentes e o caminho lógico de outros componentes dentro do documento de metadados do gravador.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Trabalhando com caminhos lógicos e de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f008b086ea50a1695a76f8b7beecab473b767fb1e2835fd5686197bb1b583175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344249"
---
# <a name="working-with-selectability-and-logical-paths"></a>Trabalhando com caminhos lógicos e de seleção

A participação de um gravador em uma operação de backup ou restauração, e quais dos seus dados são salvos, depende de quais dos seus componentes são [*incluídos explicitamente*](vssgloss-e.md) como parte do documento de componentes de backup de um solicitante e da relação entre esses componentes e o caminho lógico de outros componentes dentro do documento de metadados do gravador.

Gravadores sem componentes adicionados ao documento de componente de backup de um solicitante antes da geração de um evento [*PrepareForBackup*](vssgloss-p.md) (no caso de operações de backup) ou de um evento de [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (no caso de operações de restauração) não recebem eventos após esse ponto e não participarão da operação de backup ou restauração.

No entanto, a liberdade de um solicitante de incluir ou excluir um determinado componente em um backup ou restauração é governada pelo seguinte:

-   Qualquer hierarquia que exista entre os componentes gerenciados por um gravador e expressa por [ *caminhos lógicos*](vssgloss-l.md)
-   Se o componente é designado como [ *selecionável para backup*](vssgloss-s.md)
-   Se ele é designado como [ *selecionável para restauração*](vssgloss-s.md)
-   Se existe uma dependência explícita entre um determinado componente em um determinado gravador e outros componentes em outros gravadores

Mais informações sobre esses problemas estão nos seguintes tópicos:

-   [Caminho lógico de componentes](logical-pathing-of-components.md)
-   [Trabalhando com a seleção para backup](working-with-selectability-for-backup.md)
-   [Trabalhando com a seleção para restauração e subcomponentes](working-with-selectability-for-restore-and-subcomponents.md)
-   [Seleção e trabalho com propriedades de componente](selectability-and-working-with-component-properties.md)
-   [Dependências entre componentes gerenciados por diferentes gravadores](dependencies-between-components-managed-by-different-writers.md)

 

 



