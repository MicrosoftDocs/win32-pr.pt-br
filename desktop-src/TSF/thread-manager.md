---
title: Gerenciador de threads
description: O Gerenciador de threads é o componente base do Gerenciador do TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- TSF (estrutura de serviços de texto), Gerenciador de thread
- TSF (estrutura de serviços de texto), Gerenciador de threads
- serviços de texto, Gerenciador de threads
- Aplicativos habilitados para TSF, Gerenciador de threads
- Gerenciador de threads
- Gerenciador de TSF
- notificações de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007795"
---
# <a name="thread-manager"></a>Gerenciador de threads

O Gerenciador de threads é o componente base do Gerenciador do TSF. O Gerenciador de threads executa tarefas comuns relacionadas aos aplicativos e aos serviços de texto (clientes). Essas tarefas incluem, entre outros, a ativação e a desativação de serviços de texto do TSF, a criação de gerenciadores de documentos e a manutenção da relação apropriada entre os documentos e o foco de entrada. O Gerenciador de threads é definido pela interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .

A maioria das interfaces e dos objetos fornecidos pelo Gerenciador de TSF pode ser obtida usando os métodos fornecidos pela interface do Gerenciador de threads.

## <a name="applications"></a>Aplicativos

Um aplicativo cria um objeto do Gerenciador de threads chamando [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com CLSID \_ TFThreadMgr.

## <a name="text-services"></a>Serviços de texto

Um serviço de texto Obtém um objeto do Gerenciador de threads no método Text Service [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .

## <a name="event-notifications"></a>Notificações de eventos

O Gerenciador de threads também fornece notificação de eventos aos clientes. No TSF, as notificações de eventos são fornecidas por meio de um coletor de eventos, que é um objeto COM. Para receber notificações do Gerenciador de threads, um cliente implementa um objeto [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) e instala o coletor de eventos. O coletor de eventos é instalado consultando o Gerenciador de thread para \_ ITfSource de IID e chamando [ITfSource:: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) com IID \_ ITfThreadMgrEventSink.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor:: ativar](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource:: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 