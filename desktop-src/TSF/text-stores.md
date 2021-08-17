---
title: Armazenamentos de texto
description: Armazenamentos de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Estrutura de Serviços de Texto (TSF), armazenamentos de texto
- TSF (Estrutura de Serviços de Texto), armazenamentos de texto
- Aplicativos habilitados para TSF, armazenamentos de texto
- armazenamentos de texto
- Estrutura de Serviços de Texto (TSF), ACP (Posição do Caractere do Aplicativo)
- TSF (Estrutura de Serviços de Texto),ACP (Posição do Caractere do Aplicativo)
- Aplicativos habilitados para TSF, ACP (Posição de Caractere do Aplicativo)
- Posição do caractere do aplicativo (ACP)
- ACP (posição do caractere do aplicativo)
- Estrutura de Serviços de Texto (TSF), âncoras
- TSF (Estrutura de Serviços de Texto), âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
- Estrutura de Serviços de Texto (TSF), bloqueios de documento
- TSF (Estrutura de Serviços de Texto), bloqueios de documento
- Aplicativos habilitados para TSF, bloqueios de documentos
- bloqueios de documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af01edd439dbac23e4dee4b5289101a9bd92ca8180b66b460096b797d32b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950916"
---
# <a name="text-stores"></a>Armazenamentos de texto

## <a name="application-character-position-acp"></a>Posição do caractere do aplicativo (ACP)

Um ACP é o local de um caractere ou caracteres em um fluxo de texto expresso como o número de caracteres do início do fluxo de texto. Como o modelo ACP é baseado em zero, o primeiro caractere em um fluxo de texto tem um ACP de zero. Por exemplo:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Um repositório de texto implementa um objeto que dá suporte à interface [ITextStoreACP,](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) que permite que o fluxo de texto seja expresso em um ACP. Os métodos de interface **ITextStoreACP** usam o intervalo ACP do fluxo de texto para modificar o texto.

## <a name="anchor-based-applications"></a>Anchor-Based aplicativos

O gerente usa os métodos baseados em ACP na nativo para manipular o texto. No entanto, uma abordagem baseada em âncora está disponível para clientes do [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) que suportam [âncoras](ranges.md), em que o gerente usa métodos [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para envolver os métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink.](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)

## <a name="document-access-control"></a>Controle de acesso do documento

O armazenamento de texto controla o acesso ao fluxo de texto usando [bloqueios de documento](document-locks.md). Para ler ou modificar o repositório de texto, o gerenciador deve primeiro instalar um sink de consultoria que dê suporte à interface [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chamando o [método ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando um ponteiro para um sink de consultoria. O sink de consultoria permite que o gerenciador obtenha um bloqueio de documento no armazenamento de texto e receba notificações quando o armazenamento de texto é modificado por algo diferente do gerenciador, como a entrada do usuário por meio do aplicativo. Os sinks de consultoria serão discutidos posteriormente neste tópico.

## <a name="how-to-initialize-the-text-store"></a>Como inicializar o armazenamento de texto

Um aplicativo inicializa um armazenamento de texto concluindo as seguintes etapas:

1.  Crie um objeto de gerenciador de threads com base na interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chamando a [função CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com um ponteiro para um objeto do gerenciador de threads. A seguir está um exemplo de código de implementação de um objeto do gerenciador de threads.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Ative o objeto gerenciador de thread chamando o [método ITfThreadMgr::Activate.](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) Esse método fornece um ponteiro para um [identificador de cliente](tfclientid.md) usado para criar um objeto de contexto. O gerenciador de threads é usado para implementar um objeto do gerenciador de documentos.
3.  Crie um objeto do gerenciador de documentos com base na interface [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chamando o método [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) com um ponteiro para o objeto do gerenciador de documentos. O objeto do gerenciador de documentos é usado para implementar um objeto de contexto que é o armazenamento de texto.
4.  Crie um objeto de contexto do gerenciador de documentos chamando o método [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) com o ponteiro para o objeto de armazenamento de texto e um ponteiro para o identificador do cliente da ativação do gerenciador de threads. Veja a seguir um exemplo de criação de um objeto de contexto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Esvaia o objeto de contexto para a pilha com o [método ITfDocumentMgr::P uário.](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) Veja a seguir um exemplo de como esvalar o objeto de contexto para a pilha:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Como modificar o armazenamento de texto

O método **ITfDocumentMgr::P ken** chama **ITextStoreACP::AdviseSink** com um ponteiro para a interface do sink de consultoria para instalar um novo sink de consultoria ou modificar um sink de consultoria existente. O sink de aviso recebe notificações quando o armazenamento de texto é modificado por algo diferente do gerenciador, como entrada do usuário para o aplicativo. Os aplicativos devem chamar o método [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando o método de entrada obtém o foco. Outras notificações para o gerenciador de threads são fornecidas chamando os métodos de interface **ITextStoreACPSink** apropriados.

No entanto, os aplicativos não devem chamar os métodos de interface **ITextStoreACPSink** em resposta aos métodos de interface **ITextStoreACP.** Os aplicativos só devem chamar métodos de interface **ITextStoreACPSink** quando o repositório de texto é modificado por algo diferente do gerenciador.

O conteúdo do armazenamento de texto pode ser modificado com um estado de entrada temporário chamado de [composição](compositions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Âncoras](ranges.md)
</dt> <dt>

[Composições](compositions.md)
</dt> <dt>

[Bloqueios de documento](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[Itextstoreacp](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Acessibilidade Ativa da Microsoft](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 