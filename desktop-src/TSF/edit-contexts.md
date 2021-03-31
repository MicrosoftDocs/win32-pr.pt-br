---
title: Editar contextos
description: Editar contextos
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- TSF (estrutura de serviços de texto), editar contextos
- TSF (estrutura de serviços de texto), editar contextos
- serviços de texto, editar contextos
- Aplicativos habilitados para TSF, editar contextos
- editar contextos
- TSF (estrutura de serviços de texto), editar cookies
- TSF (estrutura de serviços de texto), editar cookies
- serviços de texto, editar cookies
- Aplicativos habilitados para TSF, editar cookies
- editar cookies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822531"
---
# <a name="edit-contexts"></a>Editar contextos

## <a name="applications"></a>Aplicativos

Para criar um contexto de edição, um aplicativo chama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).

## <a name="text-services"></a>Serviços de texto

Um serviço de texto geralmente usa o contexto de edição atualmente ativo. O contexto de edição atualmente ativo é o contexto de edição na parte superior da pilha do Gerenciador de documentos ativo. Para obter o contexto ativo no momento, um serviço de texto chama [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) para obter o Gerenciador de documentos ativo e, em seguida, chama [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) para obter o contexto de edição na parte superior da pilha.

Em alguns casos, um serviço de texto requer seu próprio contexto de edição. Para criar um contexto de edição, um serviço de texto chama **ITfDocumentMgr:: CreateContext**.

## <a name="edit-cookies"></a>Editar cookies

Muitos métodos, como [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), exigem uma maneira de identificar um contexto de edição que tem um [bloqueio de documento](document-locks.md)somente leitura ou leitura/gravação. Um bloqueio de documento é obtido por meio de uma negociação entre o Gerenciador de TSF e o aplicativo. Um serviço de texto não pode executar essa negociação diretamente. Um serviço de texto só pode obter um bloqueio solicitando uma [sessão de edição](edit-sessions.md) com um contexto específico e acesso somente leitura ou de leitura/gravação. Quando a sessão de edição é concedida, o serviço de texto é fornecido com um *cookie de edição* que identifica o contexto de edição com o acesso solicitado. Esse cookie é passado para o método para identificar o contexto de edição com o acesso apropriado.

**ITfDocumentMgr:: CreateContext** também fornece um cookie de edição para o criador de contexto. Esse cookie tem acesso somente leitura e não há como modificar o nível de acesso. Na verdade, o Gerenciador do TSF não negocia um bloqueio de documento para este cookie de edição. O cookie é marcado internamente como somente leitura, mas o documento não está realmente bloqueado. Por exemplo, se o criador de contexto chamar [ITfContext:: Getselecting](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) com o cookie de edição retornado por **ITfDocumentMgr:: CreateContext** , isso resultará na chamada de [ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) ou [ITextStoreAnchor:: getselecionation](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) do aplicativo. Antes de obter a seleção, o aplicativo determinará se existe um bloqueio de documento. Como não existe bloqueio, o aplicativo falhará com TS \_ E \_ NOLOCK. Ou seja, se um aplicativo chama um método com esse cookie que resulta em um dos métodos de armazenamento de texto do aplicativo que está sendo chamado, ele deve tratar esse caso internamente, pois o aplicativo não terá realmente um bloqueio de documento.

Se o criador de contexto exigir um cookie de edição com acesso de leitura/gravação, ele deverá estabelecer sua própria sessão de edição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[Bloqueios de documentos](document-locks.md)
</dt> <dt>

[Editar sessões](edit-sessions.md)
</dt> <dt>

[ITfContext:: getseleções](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




