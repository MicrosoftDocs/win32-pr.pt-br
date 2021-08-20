---
description: Para gerar uma caixa de diálogo que solicita que o usuário insira o próximo disco ou especifique um novo caminho de origem, chame SetupPromptForDisk.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Solicitando um disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872ca589d07afe558f4640878860c1f47e638386e6d8a6578bdf221749cfaffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965031"
---
# <a name="prompting-for-a-disk"></a>Solicitando um disco

Para gerar uma caixa de diálogo que solicita que o usuário insira o próximo disco ou especifique um novo caminho de origem, chame [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska). Essa função é usada por rotinas de retorno de chamada para gerar uma interface do usuário quando a notificação, [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md), é enviada para a rotina de retorno de chamada.

A caixa de diálogo gerada por [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) oferece ao usuário a opção de inserir um disco, especificar um novo caminho de origem ou cancelar a instalação.

Você pode usar sinalizadores especificados durante a chamada para [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) para alterar o layout e o comportamento da caixa de diálogo. Usando esses sinalizadores, você pode controlar se a caixa de diálogo inclui botões que permitem que o usuário procure um novo caminho de origem ou ignore o arquivo atual. Os sinalizadores também permitem controlar o comportamento da caixa de diálogo, como avisos quando exibidos pela primeira vez, e a capacidade de ser exibida como uma janela de primeiro plano.

 

 



