---
description: Depois de determinar como organizar o filtro por meio de uma estrutura CAPTUREFILTER, você deve alocar e preencher a estrutura, que é passada para o driver de Monitor de Rede por meio de um BLOB de configuração.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementando o código de filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837500"
---
# <a name="implementing-the-capture-filter-code"></a>Implementando o código de filtro de captura

Depois de determinar como organizar o filtro por meio de uma estrutura [**CAPTUREFILTER**](capturefilter.md) , você deve alocar e preencher a estrutura, que é passada para o driver de monitor de rede por meio de um blob de configuração.

Usuários NPP diretos adicionam o filtro de captura ao BLOB de configuração que é passado para **conectar**, [**Configurar**](configure.md)ou ambos. Para obter uma lista de interfaces COM que você pode usar para se comunicar com o NPP, consulte [interfaces NPP](npp-interfaces.md).

 

 



