---
description: O mapeador de expedição é criado usando o COM CoCreateInstance e expõe uma interface, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Mapeador de expedição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779909"
---
# <a name="dispatch-mapper"></a>Mapeador de expedição

O mapeador de expedição é criado usando o COM **CoCreateInstance** e expõe uma interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper). Essa interface permite que um aplicativo recupere o ponteiro de expedição de outra interface em um objeto, dado o ponteiro de expedição de uma interface e o GUID de outra. Essa interface é fornecida para auxiliar os programadores usando aplicativos de script que não fornecem um meio de sondagem imediata das interfaces em um objeto.

O mapeador de expedição usa a interface **IObjectSafety** de um objeto para certificar-se de que o objeto é seguro para scripts na interface solicitada. Se o objeto não implementar **IObjectSafety**, ou se o objeto não for seguro nessa interface específica, a chamada falhará.

 

 



