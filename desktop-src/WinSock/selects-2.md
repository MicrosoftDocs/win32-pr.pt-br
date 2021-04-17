---
description: Na interface de soquete do BSD (Berkeley Software Distribution) original, a função Select era o padrão (e somente) significa obter indicações de eventos de rede.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Optar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790596"
---
# <a name="selects"></a>Optar

Na interface de soquete do BSD (Berkeley Software Distribution) original, a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era o padrão (e somente) significa obter indicações de eventos de rede. Para cada soquete, as informações sobre o status de leitura, gravação ou erro podem ser sondadas ou aguardadas. Consulte [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) para obter mais informações. Observe que o evento de rede FD \_ QoS não pode ser obtido por essa abordagem.

 

 
