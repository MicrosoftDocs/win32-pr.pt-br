---
title: Manipulação de teclado para controles
description: Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26081d36c62b11163ceb8c41421ea0370d18b3ce9bf16be68e4e8a06a5f1a489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736553"
---
# <a name="keyboard-handling-for-controls"></a>Manipulação de teclado para controles

Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar ações executadas pelo controle. O contêiner gerencia a atividade de teclado para todos os seus controles inseridos. Com documentos compostos, os aceleradores de teclado se aplicam somente ao objeto ativo no momento. Com controles, um mecanismo foi adicionado para que um controle possa responder a seus mnemônicos de teclado, mesmo que ele não esteja atualmente na interface do usuário-ativo.

Os métodos [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemônico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e o método [**IOleControlSite:: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) manipulam os mnemônicos de teclado de um controle. Uma estrutura [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descreve os aceleradores mnemônicos de um controle e os sinalizadores passados com ele por meio do método **GetControlInfo** descrevem o comportamento dos controles com as teclas ENTER e ESC. Quando um controle altera seus mnemônicos, ele chama **OnControlInfoChanged** para que o contêiner possa recarregar a estrutura, se necessário.

Quando um controle está ativo na interface do usuário, ele também é o controle com o foco. Como os controles são ativados e desativados entre o ativo in-loco e os Estados ativos da interface do usuário, o controle chama [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) para informar ao contêiner de tais alterações.

Além disso, quando um controle está ativo na interface do usuário, ele terá a primeira chance de processar qualquer pressionamento de tecla. Para dar a um contêiner a oportunidade de processar o pressionamento de tecla antes do controle, o controle chama [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Se o contêiner não tratar o pressionamento de tecla, o controle o processará.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ActiveX Controles](activex-controls.md)
</dt> </dl>

 

 




