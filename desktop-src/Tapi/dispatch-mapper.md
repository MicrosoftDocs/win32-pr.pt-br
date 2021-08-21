---
description: O Dispatch Mapper é criado usando COM CoCreateInstance e expõe uma interface, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Dispatch Mapper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0880228ab608abe5f599d58bb47d211d1458dd49636a9bdc992f31dfa26c028
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118866680"
---
# <a name="dispatch-mapper"></a>Dispatch Mapper

O Dispatch Mapper é criado usando COM **CoCreateInstance** e expõe uma interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper). Essa interface permite que um aplicativo recupere o ponteiro de expedição de outra interface em um objeto, considerando o ponteiro de expedição de uma interface e o GUID de outra. Essa interface é fornecida para ajudar os programadores a usar aplicativos de script que não fornecem um meio de sondar prontamente as interfaces em um objeto.

O Dispatch Mapper usa a interface **IObjectSafety** de um objeto para garantir que o objeto seja seguro para scripts na interface solicitada. Se o objeto não implementar **IObjectSafety** ou se o objeto não estiver seguro nessa interface específica, a chamada falhará.

 

 



