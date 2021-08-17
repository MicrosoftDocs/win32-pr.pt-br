---
description: Na TAPI versão 3,0 e posterior, o modelo de objeto TAPI usa objetos de terminal para representar a origem ou o coletor de um fluxo de mídia associado a uma sessão de chamada ou de comunicação.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Objeto terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe85dcf2643cbf60835a7df9e8b20de8287da2c752ed6555f480609d9b79873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476256"
---
# <a name="terminal-object"></a>Objeto terminal

Na TAPI versão 3,0 e posterior, o modelo de objeto TAPI usa objetos de terminal para representar a origem ou o coletor de um fluxo de mídia associado a uma sessão de chamada ou de comunicação. Esse modelo de objeto permite que um aplicativo especifique, em um nível detalhado, como a mídia é processada em uma chamada. Esse modelo também permite que vários terminais sejam selecionados simultaneamente, por exemplo, uma chamada pode ser saída para um alto-falante de áudio e gravada simultaneamente.

O objeto terminal representa uma fonte ou um processador, como um microfone ou um palestrante. Um aplicativo escolhe entre os terminais disponíveis com base na direção da mídia e no tipo ou tipos envolvidos em uma sessão de comunicações. Cada fluxo de mídia associado é selecionado para o terminal apropriado a fim de iniciar o streaming.

Os terminais são normalmente implementados por um provedor de serviços de mídia (MSP) e os objetos de terminal não estarão disponíveis se não houver um MSP associado a uma sessão de comunicações. uma exceção é que, com o Windows 2000 SP1 e posterior, um aplicativo pode implementar uma forma de [terminal conectável](pluggable-terminals.md). isso permite que um servidor de conferência crie terminais de ponte para que os clientes que não são Windows 2000 SP1 ou não multicast possam ser adicionados a conferências de multicast/IP multipartes da TAPI 3.

Cada terminal pertence a uma [classe terminal](terminal-class.md). Uma classe de terminal representa um conjunto de recursos de origem ou de renderização. Por exemplo, um terminal que mapeia para um conjunto de alto-falantes de áudio seria identificado como CLSID \_ SpeakersTerminal, e o provedor de serviços deve ser a implementação do controle de volume. A TAPI 3 define um conjunto de classes de terminal, um MSP pode definir classes adicionais e um aplicativo pode registrar novas classes de terminal. Cada classe de terminal é atribuída a um GUID (identificador global exclusivo).

Do ponto de vista de um aplicativo, um terminal é descrito por seu tipo e [direção](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)de [terminal](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) . O tipo pode ser estático ou dinâmico. Um terminal estático é mapeado para hardware, como um telefone ou microfone. Um terminal dinâmico é mapeado para um objeto transitório, como um arquivo ou uma janela de vídeo. A direção descreve se um determinado terminal é uma origem ou um processador.

Os recursos de um determinado objeto terminal podem variar consideravelmente dependendo do par atual do provedor de serviços em uso. O MSP para um dispositivo especializado pode implementar uma interface com métodos apropriados para esse dispositivo. Essa interface pode ser agregada no objeto terminal e nos métodos disponibilizados para um aplicativo. Para obter mais informações e material de referência, consulte a documentação do provedor de serviços de mídia.

Para obter mais informações sobre interfaces de terminal e métodos implementados pela TAPI 3, consulte [interfaces de objeto de terminal](terminal-object-interfaces.md).

Se os autores de um provedor de serviços de mídia usarem as classes base MSP, eles poderão implementar alguns dos recursos do terminal de streaming de mídia.

Para obter mais informações e exemplos de código que mostram ilustrações de como usar um objeto de terminal, consulte [fazer uma chamada](make-a-call.md) e [receber uma chamada](receive-a-call.md).

**Windows XP:** para obter mais informações sobre como o objeto de Terminal foi expandido no Windows XP, consulte [terminais de arquivos](file-terminals.md), [terminais Multitrack](multitrack-terminals.md)e [terminais conectáveis](pluggable-terminals.md).

Para obter mais informações e exemplos de código, consulte [usando terminais de arquivo](using-file-terminals.md), [usando terminais multitrack e o mecanismo de seleção padrão](using-multitrack-terminals-and-the-default-selection-mechanism.md)e [registro de terminal conectável](pluggable-terminal-registration.md).

 

 



