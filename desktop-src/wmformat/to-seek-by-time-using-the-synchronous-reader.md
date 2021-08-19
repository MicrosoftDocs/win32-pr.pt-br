---
title: Para buscar por tempo usando o leitor síncrono
description: Para buscar por tempo usando o leitor síncrono
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- ASF (Advanced Systems Format), buscando por tempo
- ASF (formato de sistemas avançados), buscando por tempo
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, buscando por tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74fb0cb4f73e70821347b82a9e5a2544eb9759e733fb164077b2fc007163db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432629"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a>Para buscar por tempo usando o leitor síncrono

Para procurar dados usando o leitor síncrono, especifique um intervalo para reprodução. Um intervalo é definido por uma hora de apresentação inicial e uma duração, tanto em unidades de 100 nanossegundos.

Para buscar dados em um arquivo ASF por hora de apresentação usando o leitor síncrono, execute as etapas a seguir.

1.  Especifique uma hora e duração de início para a entrega de exemplo chamando [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange). Esse método não exige que você especifique um número de fluxo porque os horários de apresentação de cada fluxo já devem estar sincronizados.
2.  Comece a recuperar exemplos com chamadas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample). Prossiga normalmente com o leitor síncrono.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




