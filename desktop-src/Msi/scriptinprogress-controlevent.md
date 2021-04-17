---
description: O instalador usa esse evento para exibir uma cadeia de caracteres informativa enquanto o script de execução da instalação está sendo compilado.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749575"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent,

O instalador usa esse evento para exibir uma cadeia de caracteres informativa enquanto o script de execução da instalação está sendo compilado. A cadeia de caracteres informativa pode ser exibida em uma caixa de diálogo por um [controle de texto](text-control.md) que assina esse ControlEvent,. Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).

Esse ControlEvent, pode ser manipulado por uma interface do usuário executada na [*interface da usuário básica*](b-gly.md), na [*IU reduzida*](r-gly.md)ou em níveis [*completos da interface*](f-gly.md) de usuários. Para obter informações sobre níveis de interface do usuário, consulte [níveis de interface de usuários](user-interface-levels.md).

## <a name="published-by"></a>Publicada por

Esse ControlEvent, é publicado pelo instalador.

## <a name="argument"></a>Argumento

Nenhum.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Um [controle de texto](text-control.md) que se inscrever em ScriptInProgress exibirá a cadeia de caracteres de texto especificada na [tabela UIText](uitext-table.md).

## <a name="typical-use"></a>Usos comum

Enquanto o script de execução está sendo compilado, o instalador exibe um ProgressBar que indica o tempo restante antes do início da execução do script. O autor do pacote pode exibir uma mensagem preliminar neste momento explicando o ProgressBar. Para exibir uma mensagem preliminar, inclua um [controle de texto](text-control.md) na mesma caixa de diálogo sem janela restrita que o ProgressBar. Especifique que esse controle de texto assine o ScriptInProgress ControlEvent, por meio da [tabela EventMappings](eventmapping-table.md). Inclua uma entrada na [tabela UIText](uitext-table.md) com ScriptInProgress especificado no campo de chave. Especifique a mensagem preliminar como uma cadeia de texto no campo de texto da tabela UIText. Em seguida, durante a compilação do script, o instalador exibirá essa cadeia de caracteres dentro do controle de texto. O texto exibido desaparece assim que a compilação do script é concluída.

O mesmo controle de texto que assina o ScriptInProgress ControlEvent, também pode assinar o ControlEvent, de [permanência](timeremaining-controlevent.md). Nesse caso, como o texto da cadeia de caracteres preliminar do ScriptInProgress desaparece, ele é substituído pela cadeia de caracteres "tempo restante: XX minutos".

 

 



