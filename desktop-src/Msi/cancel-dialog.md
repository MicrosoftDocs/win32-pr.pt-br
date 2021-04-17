---
description: Uma caixa de diálogo cancelar confirma que o usuário deseja encerrar a instalação. Essa é uma caixa de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Cancelar caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749804"
---
# <a name="cancel-dialog"></a>Cancelar caixa de diálogo

Uma caixa de diálogo **Cancelar** confirma que o usuário deseja encerrar a instalação. Essa é uma caixa de diálogo modal.

Esse tipo de caixa de diálogo normalmente contém um [controle de texto](text-control.md) e dois [supressãos](pushbutton-control.md). Os dois botões dão ao usuário a opção de retornar à última caixa de diálogo ou confirmar o encerramento da instalação.

O [EndDialog](enddialog-controlevent.md) ControlEvent, está vinculado a esses dois botões na [tabela ControlEvent,](controlevent-table.md). O parâmetro de *retorno* do ControlEvent, EndDialog é vinculado a um dos botões e faz com que a caixa de diálogo **Cancelar** seja encerrada e o foco retorne à caixa de diálogo anterior. O parâmetro *Exit* é vinculado ao outro botão e faz com que a interface do usuário retorne o controle para o instalador com o código apropriado indicando que o usuário deseja sair. Em seguida, o instalador desliga e exibe a [caixa de diálogo UserExit](userexit-dialog.md).

 

 



