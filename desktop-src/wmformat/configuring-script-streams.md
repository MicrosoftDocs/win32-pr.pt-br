---
title: configurando o Script Fluxos
description: configurando o Script Fluxos
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- fluxos, configurando fluxos de script
- codecs, configurando fluxos de script
- fluxos de script, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f95c4c43fcb29ec2f77dacbf5a66b1c8c36c666d80fd5f5c09779a4ecaf22f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655984"
---
# <a name="configuring-script-streams"></a>configurando o Script Fluxos

Como todos os tipos de fluxo arbitrários, os fluxos de script precisam ter uma taxa de bits e uma janela de buffer definidas para eles. O tipo de mídia principal na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve ser definido como WMMEDIATYPE \_ script.

Fluxos de script precisam ter o membro **formatType** do **\_ \_ tipo de mídia do WM** definido como WMFORMAT \_ script, que indica que o membro **pbFormat** aponta para uma estrutura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .

Há apenas um tipo de script com suporte, WMSCRIPTTYPE \_ TwoStrings.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> </dl>

 

 




