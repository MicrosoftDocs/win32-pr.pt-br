---
title: Como funcionam as notificações
description: Como funcionam as notificações
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756366"
---
# <a name="how-notifications-work"></a>Como funcionam as notificações

As notificações se originam no aplicativo de objeto e fluem para o contêiner por meio do manipulador de objetos. Se o objeto for um objeto vinculado, o objeto vinculado interceptará as notificações do manipulador de objetos e notificará o contêiner diretamente.

Um aplicativo de objeto deve gerenciar solicitações de registro, mantendo o controle de onde enviar quais notificações e enviar essas notificações quando apropriado. O OLE fornece dois objetos de componente para simplificar essa tarefa: o OleAdviseHolder para notificações compostas de documentos e o DataAdviseHolder para notificações de dados.

Os aplicativos de objeto determinam as condições que solicitam o envio de cada notificação específica e a frequência com que cada notificação deve ser enviada. Quando for apropriado enviar várias notificações, não importa qual notificação será enviada primeiro; eles podem ser enviados em qualquer ordem.

O tempo das notificações afeta o desempenho e a coordenação entre um aplicativo de objeto e seus contêineres. Enquanto as notificações enviadas com muita frequência e processamento lento, as notificações enviadas com pouca frequência resultam em um contêiner fora de sincronização. A frequência de notificação pode ser comparada com a taxa na qual um aplicativo é reintint. Portanto, usar lógica semelhante para o tempo de notificações (como é usado para repintar) é inteligente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**Createoleadviseholder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notificações](notifications.md)
</dt> </dl>

 

 