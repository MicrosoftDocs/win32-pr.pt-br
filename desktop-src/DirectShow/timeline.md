---
description: Linha do tempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787126"
---
# <a name="timeline"></a>Linha do tempo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O objeto Timeline gerencia todos os objetos em um projeto de edição de vídeo. Para criar esse objeto, chame **CoCreateInstance**. O identificador de classe é CLSID \_ AMTimeline.

Para ler arquivos do Windows Media™, o aplicativo deve fornecer um certificado de software, também chamado de chave. Registre o aplicativo como um provedor de chaves por meio da interface **IObjectWithSite** da linha do tempo. Para obter mais informações, consulte [desbloqueando o SDK do Windows Media Format](unlocking-the-windows-media-format-sdk.md).

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

 

 



