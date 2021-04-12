---
title: Como as notificações funcionam
description: Como as notificações funcionam
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366777"
---
# <a name="how-notifications-work"></a>Como as notificações funcionam

As notificações são originadas no aplicativo de objeto e fluem para o contêiner por meio do manipulador de objetos. Se o objeto for um objeto vinculado, o objeto vinculado interceptará as notificações do manipulador de objetos e notificará o contêiner diretamente.

Um aplicativo de objeto deve gerenciar solicitações de registro, controlando para onde enviar as notificações e enviá-las quando apropriado. O OLE fornece dois objetos de componente para simplificar esta tarefa: o OleAdviseHolder para notificações de documentos compostos e o DataAdviseHolder para notificações de dados.

Os aplicativos de objeto determinam as condições que solicitam o envio de cada notificação específica e a frequência com a qual cada notificação deve ser enviada. Quando for apropriado que várias notificações sejam enviadas, não importa qual notificação é enviada primeiro; Eles podem ser enviados em qualquer ordem.

O tempo das notificações afeta o desempenho e a coordenação entre um aplicativo de objeto e seus contêineres. Enquanto as notificações são enviadas com muito frequência, as notificações enviadas com pouca frequência resultam em um contêiner fora de sincronia. A frequência de notificação pode ser comparada com a taxa de repintura de um aplicativo. Portanto, usar uma lógica semelhante para o tempo das notificações (como é usado para repintura) é inteligente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notificações](notifications.md)
</dt> </dl>

 

 