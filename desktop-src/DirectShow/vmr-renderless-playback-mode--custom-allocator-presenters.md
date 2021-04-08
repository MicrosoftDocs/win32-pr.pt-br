---
description: Modo de reprodução do VMR (alocador personalizado-apresentadores)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modo de reprodução do VMR (alocador personalizado-apresentadores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662544"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>Modo de reprodução do VMR (alocador personalizado-apresentadores)

No modo de reprodução de renderização, o VMR não executa a renderização. Em vez disso, ele usa um apresentador de alocador personalizado fornecido pelo aplicativo. Esse modo é útil para jogos e outros tipos de aplicativos que têm efeitos de vídeo sofisticados. O modo de reprodução sem renderização permite que os aplicativos criem e controlem sua própria superfície do DirectDraw (VMR-7) ou a superfície do Direct3D (VMR-9) e acessem os bits de vídeo no momento da apresentação.

No modo de processamento, o VMR-9 não carrega automaticamente seu componente de mixer.

No modo de reprodução de renderização, o aplicativo executa as seguintes tarefas:

-   Gerencia a janela de reprodução.
-   Aloca o objeto DirectDraw ou Direct3D e o buffer de quadro final.
-   Notifica o restante do sistema de reprodução do objeto que está sendo usado.
-   Apresenta o buffer de quadro no horário correto.
-   Lida com todas as alterações no modo de resolução, monitore alterações e perdas de superfície. Ele deve aconselhar o restante do sistema de reprodução desses eventos.

O VMR faz o seguinte:

-   Manipula todo o tempo relacionado à apresentação do quadro de vídeo.
-   Fornece informações de controle de qualidade para o aplicativo e o restante do sistema de reprodução.
-   Apresenta uma interface consistente para os componentes upstream do sistema de reprodução, que não sabem que o aplicativo está fornecendo a alocação de buffer de quadro e realizando a renderização.
-   Fornece qualquer combinação de fluxos de vídeo que podem ser necessários antes da renderização.

Como o desentrelaçamento é executado pelo mixer, o apresentador de alocador sempre recebe quadros desentrelaçados. Para obter mais informações, consulte [definindo preferências de desentrelaçamento](setting-deinterlace-preferences.md).

Para obter mais informações sobre como fornecer um apresentador de alocador personalizado, consulte os seguintes tópicos:

-   [Fornecendo um Allocator-Presenter personalizado para o VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Fornecendo um Allocator-Presenter personalizado para o VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Sincronizando o VMR com a taxa de atualização do monitor](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



