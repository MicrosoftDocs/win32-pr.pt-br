---
title: Manipulação de teclado para controles
description: Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar as ações executadas pelo controle .
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

Um controle responde aos aceleradores de teclado para que o usuário final possa iniciar as ações executadas pelo controle . O contêiner gerencia a atividade de teclado para todos os seus controles inseridos. Com documentos compostos, os aceleradores de teclado se aplicam somente ao objeto ativo no momento. Com controles, um mecanismo foi adicionado para que um controle possa responder a seus mnemônicos de teclado, mesmo que ele não seja ativo na interface do usuário no momento.

Os métodos [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e o [**método IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) lidam com mnemônicos de teclado de um controle. Uma [**estrutura CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descreve os aceleradores mnemônicos de um controle e os sinalizadores passados com ele por meio do método **GetControlInfo** descrevem o comportamento de controles com as teclas Enter e Esc. Quando um controle altera seus mnemônicos, ele chama **OnControlInfoChanged** para que o contêiner possa recarregar a estrutura, se necessário.

Quando um controle está ativo na interface do usuário, ele também é o controle com o foco. À medida que os controles são ativados e desativados entre os estados ativos in-loco e da interface do usuário, o controle chama [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) para dizer ao contêiner sobre essas alterações.

Além disso, quando um controle estiver ativo na interface do usuário, ele terá a primeira chance de processar quaisquer teclas de tecla. Para dar a um contêiner a oportunidade de processar o soquete de teclas antes do controle, o controle chama [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Se o contêiner não manipular o controle de teclas, o controle o processa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ActiveX Controles](activex-controls.md)
</dt> </dl>

 

 




