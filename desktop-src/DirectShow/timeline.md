---
description: Linha do tempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651248"
---
# <a name="timeline"></a>Linha do tempo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto Timeline gerencia todos os objetos em um projeto de edição de vídeo. Para criar esse objeto, chame **CoCreateInstance**. O identificador de classe é CLSID \_ AMTimeline.

para ler arquivos de™ de mídia Windows, o aplicativo deve fornecer um certificado de software, também chamado de chave. Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** da linha do tempo. para obter mais informações, consulte [desbloqueando o SDK do formato de mídia Windows](unlocking-the-windows-media-format-sdk.md).

O objeto Timeline expõe as seguintes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O modelo de linha do tempo](the-timeline-model.md)
</dt> <dt>

[Construindo uma linha do tempo](constructing-a-timeline.md)
</dt> </dl>

 

 



