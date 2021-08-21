---
title: Gerenciador de Threads
description: O gerenciador de threads é o componente base do gerenciador do TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Estrutura de Serviços de Texto (TSF), gerenciador de threads
- TSF (Estrutura de Serviços de Texto), gerenciador de threads
- serviços de texto, gerenciador de threads
- Aplicativos habilitados para TSF, gerenciador de threads
- gerenciador de threads
- Gerenciador do TSF
- notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55452ee6102232023c9d544e2207693df962dc6c2d83b23c95b0a119402da884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874037"
---
# <a name="thread-manager"></a>Gerenciador de Threads

O gerenciador de threads é o componente base do gerenciador do TSF. O gerenciador de threads executa tarefas comuns relacionadas a aplicativos e serviços de texto (clientes). Essas tarefas incluem, mas não se limitam à ativação e desativação de serviços de texto TSF, a criação de gerenciadores de documentos e a manutenção da relação adequada entre documentos e o foco de entrada. O gerenciador de threads é definido pela interface [ITfThreadMgr.](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)

A maioria das interfaces e objetos fornecidos pelo gerenciador de TSF pode ser obtida usando os métodos fornecidos pela interface do gerenciador de threads.

## <a name="applications"></a>Aplicativos

Um aplicativo cria um objeto de gerenciador de thread chamando [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com CLSID \_ TFThreadMgr.

## <a name="text-services"></a>Serviços de Texto

Um serviço de texto obtém um objeto de gerenciador de threads no método [ITfTextInputProcessor::Activate do](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) serviço de texto.

## <a name="event-notifications"></a>Notificações de eventos

O gerenciador de threads também fornece notificação de eventos para clientes. No TSF, as notificações de eventos são fornecidas por meio de um sink de evento, que é um objeto COM. Para receber notificações do gerenciador de threads, um cliente implementa um objeto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e instala o sink do evento. O sink de eventos é instalado consultando o gerenciador de threads para \_ IID ITfSource e chamando [ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) com \_ IID ITfThreadMgrEventSink.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[Cocreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource::AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 