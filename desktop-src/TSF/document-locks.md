---
title: Bloqueios de documentos
description: Bloqueios de documentos
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- TSF (estrutura de serviços de texto), bloqueios de documentos
- TSF (estrutura de serviços de texto), bloqueios de documentos
- Aplicativos habilitados para TSF, bloqueios de documentos
- bloqueios de documentos
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- Aplicativos habilitados para TSF, posição de caracteres do aplicativo (ACP)
- Posição de caracteres do aplicativo (ACP)
- ACP (posição do caractere do aplicativo)
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159567"
---
# <a name="document-locks"></a>Bloqueios de documentos

## <a name="the-document-lock-protocol"></a>O protocolo de bloqueio de documento

Para solicitar um bloqueio de documento para aplicativos baseados em ACP, o Gerenciador de TSF chama [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock). Para aplicativos baseados em ancoragem, o Gerenciador TSF chama [ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock). O aplicativo concede o bloqueio de documento chamando [ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (aplicativos baseados em ACP) ou [ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (aplicativos baseados em âncora) dentro de **RequestLock**. O bloqueio só é válido durante a chamada **OnLockGranted** . Quando **OnLockGranted** retorna, o documento é considerado desbloqueado.

## <a name="types-of-document-locks"></a>Tipos de bloqueios de documento

Há dois tipos de bloqueios de documentos, somente leitura e leitura/gravação. Um bloqueio somente leitura permite que o gerente Leia o texto, mas não pode modificar ou inserir texto. Um bloqueio de leitura/gravação permite que o gerente Leia, modifique e insira texto. Um bloqueio somente leitura é solicitado por meio da especificação \_ de TS LF \_ lido no *dwFlags*. Um bloqueio de leitura/gravação é solicitado pela especificação \_ de TS LF \_ ReadWrite no *dwFlags*.

## <a name="asynchronous-and-synchronous-requests"></a>Solicitações assíncronas e síncronas

Uma solicitação de bloqueio pode ser síncrona ou assíncrona. O gerente solicita um bloqueio síncrono usando o sinalizador de \_ sincronização TS LF \_ no *dwFlags*. Se esse sinalizador não estiver presente, a solicitação será assíncrona.

## <a name="granting-the-lock"></a>Concedendo o bloqueio

Quando **RequestLock** é chamado, o aplicativo deve determinar se o documento está bloqueado no momento. Se o documento não estiver bloqueado e nenhum outro motivo para negar o bloqueio existir, o aplicativo deverá definir *phrSession* como s \_ OK e retornar s \_ OK.

Se o documento estiver bloqueado e a solicitação de bloqueio for síncrona, o aplicativo deverá definir *phrSession* como TS \_ e \_ síncrono e retornar S \_ OK. Isso indica que uma solicitação síncrona não pode ser concedida.

Se o documento estiver bloqueado e a solicitação de bloqueio for assíncrona, o aplicativo deverá enfileirar a solicitação, definir *phrSession* como TS \_ S \_ Async e retornar S \_ OK. Quando o documento estiver disponível, o aplicativo deverá remover a solicitação da fila e chamar **OnLockGranted**. Esse enfileiramento de solicitações de bloqueio é opcional; Há um cenário ao qual um aplicativo deve dar suporte. Se o documento tiver um bloqueio somente leitura, a nova solicitação de bloqueio será leitura/gravação e a solicitação será assíncrona, o aplicativo terá se chamado em **OnLockGranted** , o que causou uma chamada reentrante para **RequestLock**. O aplicativo deve definir *phrSession* como TS \_ S \_ Async e retornar S \_ OK. Depois que a chamada para **OnLockGranted** retorna, o aplicativo deve processar a solicitação de atualização chamando **ONLOCKGRANTED** novamente com TS \_ LF \_ ReadWrite.

## <a name="lock-enforcement"></a>Imposição de bloqueio

O aplicativo deve garantir que o tipo apropriado de bloqueio exista antes de permitir o acesso ao documento. Por exemplo, o aplicativo deve verificar se um documento tem pelo menos um bloqueio somente leitura antes de permitir [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) para continuar. Se o bloqueio apropriado não existir, o aplicativo deverá retornar TF \_ E \_ NOLOCK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Armazenamentos de texto](text-stores.md)
</dt> <dt>

[ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[ITextStoreACPSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[ITextStoreAnchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[ITextStoreAnchorSink:: OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




