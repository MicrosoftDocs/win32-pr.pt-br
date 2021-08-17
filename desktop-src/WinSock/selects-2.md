---
description: Na interface de soquete do BSD (Berkeley Software Distribution) original, a função Select era o padrão (e somente) significa obter indicações de eventos de rede.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Optar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740918"
---
# <a name="selects"></a>Optar

Na interface de soquete do BSD (Berkeley Software Distribution) original, a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era o padrão (e somente) significa obter indicações de eventos de rede. Para cada soquete, as informações sobre o status de leitura, gravação ou erro podem ser sondadas ou aguardadas. Consulte [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) para obter mais informações. Observe que o evento de rede FD \_ QoS não pode ser obtido por essa abordagem.

 

 
