---
description: Métodos virtuais puros CMSPCallBase-esses métodos devem ser substituídos por classes derivadas.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuais puros CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094454"
---
# <a name="cmspcallbase-pure-virtual-methods"></a>Métodos virtuais puros CMSPCallBase

Esses métodos devem ser substituídos por classes derivadas.



| Métodos virtuais puros CMSPCallBase                                 | Descrição                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**MSPCallAddRef**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | Método AddRef privado para o objeto de chamada.                                                                                              |
| [**MSPCallRelease**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | Método de liberação particular para o objeto de chamada.                                                                                             |
| [**Init**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | Chamado pelo objeto de endereço MSP (no método [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar o objeto de chamada msp. |
| [**Desligar**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | Chamado pelo objeto de endereço MSP para desligar a chamada..                                                                                |
| [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | Chamado por [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para criar um objeto de fluxo.                                               |
| [**Createstreamobject**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | Chamado por [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) para criar um objeto de fluxo.                                  |
| [**RemoveStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | Chamado pelo aplicativo para remover um fluxo da chamada                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
