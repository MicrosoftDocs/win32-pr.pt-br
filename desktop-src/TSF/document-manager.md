---
title: Gerenciador de documentos
description: Gerenciador de documentos
ms.assetid: e30087b6-524a-481e-845d-0348bac3830a
keywords:
- TSF (estrutura de serviços de texto), Gerenciador de documentos
- TSF (estrutura de serviços de texto), Gerenciador de documentos
- serviços de texto, Gerenciador de documentos
- Aplicativos habilitados para TSF, Gerenciador de documentos
- Gerenciador de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc2182782218ad6a8aa0a70f296f639560307249
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635373"
---
# <a name="document-manager"></a>Gerenciador de documentos

## <a name="applications"></a>Aplicativos

Para criar um objeto do Gerenciador de documentos, um aplicativo chama [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr). O aplicativo cria um objeto separado do Gerenciador de documentos para cada documento individual que o aplicativo mantém. O aplicativo usa o Gerenciador de documentos para criar contextos de edição, adicionar um contexto à pilha de contexto e remover um contexto da pilha de contexto.

## <a name="text-services"></a>Serviços de texto

Um serviço de texto nunca cria um objeto do Gerenciador de documentos. Em vez disso, o serviço de texto Obtém o objeto do Gerenciador de documentos ativo no momento chamando [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus). Um serviço de texto usa o Gerenciador de documentos para obter o contexto na parte superior da pilha.

Um serviço de texto também pode usar o Gerenciador de documentos para criar seu próprio contexto e adicioná-lo e removê-lo da pilha de contexto. Isso normalmente é feito quando o serviço de texto deve exibir uma interface do usuário modal, como quando uma lista de palavras é exibida para permitir que o usuário selecione uma palavra. Quando a lista é exibida, o serviço de texto coloca seu próprio contexto na pilha. Quando a lista de palavras é ignorada, o serviço de texto remove seu contexto da pilha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> </dl>

 

 




