---
description: No TAPI versão 3.0 e posterior, o modelo de objeto TAPI usa objetos de terminal para representar a origem ou o sink de um fluxo de mídia associado a uma chamada ou sessão de comunicação.
ms.assetid: 0d96f229-76c0-46a3-bc4b-6f558b9956c6
title: Objeto Terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe85dcf2643cbf60835a7df9e8b20de8287da2c752ed6555f480609d9b79873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476256"
---
# <a name="terminal-object"></a>Objeto Terminal

No TAPI versão 3.0 e posterior, o modelo de objeto TAPI usa objetos de terminal para representar a origem ou o sink de um fluxo de mídia associado a uma chamada ou sessão de comunicação. Esse modelo de objeto permite que um aplicativo especifique, em um nível detalhado, como a mídia é processada em uma chamada. Esse modelo também permite que vários terminais sejam selecionados simultaneamente, portanto, por exemplo, uma chamada pode ser saída para um alto-falante de áudio e gravada simultaneamente.

O objeto Terminal representa uma origem ou renderização, como um microfone ou um alto-falante. Um aplicativo escolhe entre os terminais disponíveis com base na direção da mídia e no tipo ou tipos envolvidos em uma sessão de comunicação. Cada fluxo de mídia associado é selecionado no terminal apropriado para iniciar o streaming.

Os terminais normalmente são implementados por um MSP (provedor de serviços de mídia) e os objetos de terminal não estarão disponíveis se não houver nenhum MSP associado a uma sessão de comunicação. Uma exceção é que, com Windows 2000 SP1 e posterior, um aplicativo pode implementar uma forma de [terminal plug-able](pluggable-terminals.md). Isso permite que um servidor de conferência crie terminais de ponte para que clientes não Windows 2000 SP1 ou não multicast H323 possam ser adicionados a conferências multicast SDP/IP multicast tapi 3.

Cada terminal pertence a uma [classe de terminal](terminal-class.md). Uma classe de terminal representa um conjunto de recursos de origem ou renderização. Por exemplo, um terminal que mapeia para um conjunto de alto-falantes de áudio seria identificado como Alto-falantes CLSIDTerminal e o provedor de serviços deve \_ implementar o controle de volume. TAPI 3 define um conjunto de classes de terminal, um MSP pode definir classes adicionais e um aplicativo pode registrar novas classes de terminal. Cada classe de terminal recebe um GUID (identificador global exclusivo).

Do ponto de vista de um aplicativo, um terminal é descrito por seu [tipo de terminal e](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_type) [direção](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction). O tipo pode ser estático ou dinâmico. Um terminal estático é mapeado para hardware, como um telefone ou microfone. Um terminal dinâmico é mapeado para um objeto transitório, como um arquivo ou uma janela de vídeo. A direção descreve se um determinado terminal é uma origem ou um renderdor.

Os recursos de um determinado objeto de terminal podem variar consideravelmente dependendo do par atual do provedor de serviços em uso. O MSP para um dispositivo especializado pode implementar uma interface com métodos apropriados para esse dispositivo. Essa interface pode ser agregada ao objeto terminal e os métodos disponibilizados para um aplicativo. Para obter mais informações e material de referência, consulte a documentação do provedor de serviços de mídia.

Para obter mais informações sobre interfaces de terminal e métodos implementados pela TAPI 3, consulte [Interfaces de objeto de terminal](terminal-object-interfaces.md).

Se os autores de um provedor de serviços de mídia usarem as Classes Base do MSP, eles poderão implementar alguns dos recursos do Terminal de Streaming de Mídia.

Para obter mais informações e exemplos de código que mostram ilustrações do uso de um objeto Terminal, consulte [Fazer uma chamada](make-a-call.md) e receber uma [chamada](receive-a-call.md).

**Windows XP:** Para obter mais informações sobre como o objeto Terminal foi expandido no Windows XP, consulte Terminais de [arquivo,](file-terminals.md) [terminais multitrack](multitrack-terminals.md)e [Terminais plugáveis](pluggable-terminals.md).

Para obter mais informações e exemplos de código, consulte Using [File Terminals](using-file-terminals.md), [Using Multitrack Terminals](using-multitrack-terminals-and-the-default-selection-mechanism.md)and the Default Selection Mechanism e [Pluggable Terminal Registration](pluggable-terminal-registration.md).

 

 



