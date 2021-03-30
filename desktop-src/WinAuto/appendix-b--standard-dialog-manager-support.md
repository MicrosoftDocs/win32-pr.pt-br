---
title: Apêndice B suporte do Gerenciador de diálogo padrão
description: O Microsoft Acessibilidade Ativa fornece suporte completo para controles da caixa de diálogo do SDM (Gerenciador de caixas de diálogo padrão).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636024"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Apêndice B: suporte padrão do Gerenciador de diálogo

O Microsoft Acessibilidade Ativa fornece suporte completo para controles da caixa de diálogo do SDM (Gerenciador de caixas de diálogo padrão). O SDM é uma biblioteca de código interna da Microsoft que fornece aos aplicativos da Microsoft um grau de independência das diferenças entre os sistemas operacionais Macintosh e Microsoft Windows. O SDM é usado principalmente para caixas de diálogo no Microsoft Excel e no Microsoft Word.

O SDM apresenta problemas de auxílios de acessibilidade porque usa implementações não padrão de caixas de diálogo. Por exemplo, os botões da caixa de diálogo SDM não usam o identificador da janela da mesma forma que os elementos da interface do usuário padrão. Não é possível enviar mensagens para botões e botões não contidos na lista de janelas. Um aplicativo que usa o SDM se comunica com o controle por meio de uma interface privada.

A ilustração a seguir mostra uma caixa de diálogo de exemplo do Word. Embora pareça uma caixa de diálogo normal do Windows que usa o controle guia, é realmente uma caixa de diálogo SDM.

![captura de tela da caixa de diálogo opções com a guia Exibir selecionada](images/dialog.gif)

 

 




