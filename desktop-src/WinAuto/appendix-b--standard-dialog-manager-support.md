---
title: Apêndice B Suporte do Gerenciador de Caixas de Diálogo Padrão
description: Microsoft Active Accessibility oferece suporte completo para controles de caixa de diálogo do SDM (Gerenciador de Diálogo Padrão).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b6500cabf4820fffe12b7ef160f2e494e43db067f6b96409dee02bbfd6119e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326813"
---
# <a name="appendix-b-standard-dialog-manager-support"></a>Apêndice B: Suporte do Gerenciador de Caixas de Diálogo Standard

Microsoft Active Accessibility oferece suporte completo para controles de caixa de diálogo do SDM (Gerenciador de Diálogo Padrão). O SDM é uma biblioteca de códigos interna da Microsoft que fornece aos aplicativos da Microsoft um grau de independência das diferenças entre os sistemas operacionais Macintosh e Microsoft Windows. O SDM é usado principalmente para caixas de diálogo Microsoft Excel e Microsoft Word.

O SDM apresenta problemas para auxiliares de acessibilidade porque usa implementações não padrão de caixas de diálogo. Por exemplo, os botões da caixa de diálogo do SDM não usam os controles de janela da mesma maneira que os elementos de interface do usuário padrão. Você não pode enviar mensagens para botões e os botões não estão contidos na lista de janelas. Um aplicativo que usa o SDM se comunica com o controle por meio de uma interface privada.

A ilustração a seguir mostra uma caixa de diálogo de exemplo do Word. Embora se pareça com uma caixa Windows caixa de diálogo regular que usa o controle de tabulação, é realmente uma caixa de diálogo SDM.

![captura de tela da caixa de diálogo opções com a guia Exibição selecionada](images/dialog.gif)

 

 




