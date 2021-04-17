---
description: Para gerar uma caixa de diálogo que solicita ao usuário para inserir o próximo disco ou especificar um novo caminho de origem, chame SetupPromptForDisk.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Solicitando um disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749444"
---
# <a name="prompting-for-a-disk"></a>Solicitando um disco

Para gerar uma caixa de diálogo que solicita ao usuário para inserir o próximo disco ou especificar um novo caminho de origem, chame [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska). Essa função é usada por rotinas de retorno de chamada para gerar uma interface do usuário quando a notificação, [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md), é enviada para a rotina de retorno de chamada.

A caixa de diálogo gerada por [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) dá ao usuário a opção de inserir um disco, especificar um novo caminho de origem ou cancelar a instalação.

Você pode usar sinalizadores especificados durante a chamada para [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) para alterar o layout e o comportamento da caixa de diálogo. Usando esses sinalizadores, você pode controlar se a caixa de diálogo inclui botões que permitem ao usuário procurar um novo caminho de origem ou ignorar o arquivo atual. Os sinalizadores também permitem que você controle o comportamento da caixa de diálogo, como emitir um aviso sonoro quando exibido pela primeira vez, e a capacidade de ser exibida como uma janela em primeiro plano.

 

 



