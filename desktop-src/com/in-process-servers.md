---
title: Servidores In-Process
description: Servidores In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159773"
---
# <a name="in-process-servers"></a>Servidores In-Process

Se você implementar um aplicativo de servidor OLE como um servidor em processo — uma DLL em execução no espaço de processo do aplicativo de contêiner — e não como um servidor local — um EXE em execução em seu próprio espaço de processo — a comunicação entre o contêiner e o servidor é simplificada porque a comunicação entre os dois pode assumir a forma de chamadas de função normais. As chamadas de procedimento remoto não são necessárias porque os dois aplicativos são executados no mesmo espaço de processo. Como esperado, os objetos que gerenciam o marshaling de parâmetros também são desnecessários, embora possam ser agregados dentro da DLL sem interferir na comunicação entre o contêiner e o servidor.

Quando um aplicativo de servidor OLE é implementado como um servidor em processo, um manipulador de objeto separado não é necessário porque o próprio servidor reside no espaço de processo do cliente. A principal diferença entre um servidor em processo e o manipulador de objetos é que o servidor é capaz de gerenciar o objeto em um estado de execução enquanto o manipulador não pode. Uma consequência dessa diferença é que um servidor deve fornecer uma interface do usuário para manipular o objeto em execução, enquanto um manipulador Delega esse requisito ao servidor do objeto. Ao criar um servidor em processo, você pode agregar no manipulador padrão OLE, permitindo que ele lide com tarefas básicas, como exibição, armazenamento e notificações enquanto você implementa apenas os serviços que o manipulador não fornece ou não implementa da maneira que você precisa.

Para mais informações, consulte os seguintes tópicos:

-   [Vantagens](advantages.md)
-   [Desvantagens](disadvantages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Documentos compostos](compound-documents.md)
</dt> </dl>

 

 




