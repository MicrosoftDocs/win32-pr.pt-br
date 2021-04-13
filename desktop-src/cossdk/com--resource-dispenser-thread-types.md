---
description: Tipos de thread do dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de thread do dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370395"
---
# <a name="com-resource-dispenser-thread-types"></a>Tipos de thread do dispensador de recursos COM+

Chamadas em um dispensador de recursos COM+ podem se originar em um dos seguintes tipos de thread:

-   Thread apartment (STA)
-   Thread gratuito (MTA)
-   Thread não COM (aplicativo ou o thread do coletor de lixo do [Gerenciador do dispensador](com--dispenser-manager.md) )

Se um dispensador de recurso não for um objeto COM, ele deverá ser capaz de lidar com chamadas que chegam de qualquer thread a qualquer momento. Se um dispensador de recurso for um objeto COM, o objeto COM deverá ser registrado com um modelo de threading de **ambos**. Isso permite que threads STA ou MTA criem e usem o dispensador de recurso sem uma opção de thread.

Se um dispensador de recurso criar e usar outro objeto COM (por exemplo, um Gerenciador de recursos fora de processo), o dispensador de recursos poderá precisar manter vários proxies para esse outro objeto COM e garantir que as chamadas para o objeto sejam feitas usando o proxy apropriado para o thread de chamada. Quando o dispensador de recurso cria esse objeto, ele realiza marshaling e salva a referência. Antes de chamar o objeto novamente, ele deve ser desempacotado para criar um proxy para o thread de chamada.

Pode ser mais eficiente armazenar em cache esses proxies por thread, mantendo um mapa da ID do thread para um ponteiro de proxy. Esse mapa se expande conforme novos threads são usados no processo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



