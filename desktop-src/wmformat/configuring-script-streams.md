---
title: Configurando fluxos de script
description: Configurando fluxos de script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- fluxos, configurando fluxos de script
- codecs, configurando fluxos de script
- fluxos de script, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005391"
---
# <a name="configuring-script-streams"></a>Configurando fluxos de script

Como todos os tipos de fluxo arbitrários, os fluxos de script precisam ter uma taxa de bits e uma janela de buffer definidas para eles. O tipo de mídia principal na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve ser definido como WMMEDIATYPE \_ script.

Fluxos de script precisam ter o membro **formatType** do **\_ \_ tipo de mídia do WM** definido como WMFORMAT \_ script, que indica que o membro **pbFormat** aponta para uma estrutura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

Há apenas um tipo de script com suporte, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> </dl>

 

 




