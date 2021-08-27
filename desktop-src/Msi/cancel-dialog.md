---
description: Uma caixa de diálogo Cancelar confirma que o usuário deseja encerrar a instalação. Essa é uma caixa de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Caixa de diálogo Cancelar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2f0ba12c442b8b0f4445077497c26649b79714d1a1d77af7b2a82e6c1a3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105386"
---
# <a name="cancel-dialog"></a>Caixa de diálogo Cancelar

Uma **caixa de** diálogo Cancelar confirma que o usuário deseja encerrar a instalação. Essa é uma caixa de diálogo modal.

Esse tipo de caixa de diálogo geralmente contém um [controle Texto](text-control.md) e dois [PushButtons.](pushbutton-control.md) Os dois botões dão ao usuário a opção de retornar à última caixa de diálogo ou confirmar o encerramento da instalação.

O [EndDialog](enddialog-controlevent.md) ControlEvent está vinculado a esses dois botões na [tabela ControlEvent](controlevent-table.md). O *parâmetro Return* do EndDialog ControlEvent é vinculado a  um dos botões e faz com que a caixa de diálogo Cancelar seja encerrada e o foco retorne à caixa de diálogo anterior. O *parâmetro Exit* está vinculado ao outro botão e faz com que a interface do usuário retorne o controle ao instalador com o código apropriado que indica que o usuário deseja sair. Em seguida, o instalador é desligado e exibe a [Caixa de Diálogo UserExit](userexit-dialog.md).

 

 



