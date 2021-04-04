---
title: Armazenamentos de texto
description: Armazenamentos de texto
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- TSF (estrutura de serviços de texto), armazenamentos de texto
- TSF (estrutura de serviços de texto), armazenamentos de texto
- Aplicativos habilitados para TSF, armazenamentos de texto
- armazenamentos de texto
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- TSF (estrutura de serviços de texto), função de caractere do aplicativo (ACP)
- Aplicativos habilitados para TSF, posição de caracteres do aplicativo (ACP)
- Posição de caracteres do aplicativo (ACP)
- ACP (posição do caractere do aplicativo)
- TSF (estrutura de serviços de texto), âncoras
- TSF (estrutura de serviços de texto), âncoras
- Aplicativos habilitados para TSF, âncoras
- âncoras
- TSF (estrutura de serviços de texto), bloqueios de documentos
- TSF (estrutura de serviços de texto), bloqueios de documentos
- Aplicativos habilitados para TSF, bloqueios de documentos
- bloqueios de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007738"
---
# <a name="text-stores"></a>Armazenamentos de texto

## <a name="application-character-position-acp"></a>Posição de caracteres do aplicativo (ACP)

Um ACP é o local de um caractere, ou caracteres, em um fluxo de texto que é expresso como o número de caracteres desde o início do fluxo de texto. Como o modelo ACP é baseado em zero, o primeiro caractere em um fluxo de texto tem um ACP igual a zero. Por exemplo:


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



Um armazenamento de texto implementa um objeto que dá suporte à interface [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) , que permite que o fluxo de texto seja expresso em um ACP. Os métodos de interface **ITextStoreACP** usam o intervalo de ACP do fluxo de texto para modificar o texto.

## <a name="anchor-based-applications"></a>Anchor-Based aplicativos

O Gerenciador usa os métodos baseados em ACP nativamente para manipular o texto. No entanto, uma abordagem baseada em âncora está disponível para clientes do [Microsoft acessibilidade ativa](../winauto/microsoft-active-accessibility.md) que dão suporte a [âncoras](ranges.md), no qual o gerente usa métodos [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) e [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) para encapsular os métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) .

## <a name="document-access-control"></a>Controle de acesso a documentos

O armazenamento de texto controla o acesso ao fluxo de texto usando [bloqueios de documento](document-locks.md). Para ler ou modificar o armazenamento de texto, o gerente deve primeiro instalar um coletor de aviso que dê suporte à interface [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) chamando o método [ITextStoreACP:: AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) e passando um ponteiro para um coletor de aviso. O coletor de aviso permite que o gerente obtenha bloqueios de documentos no armazenamento de texto e receba notificações quando o armazenamento de texto for modificado por algo diferente do gerente, como entrada do usuário por meio do aplicativo. Os coletores de aviso são discutidos posteriormente neste tópico.

## <a name="how-to-initialize-the-text-store"></a>Como inicializar o armazenamento de texto

Um aplicativo Inicializa um repositório de texto concluindo as seguintes etapas:

1.  Crie um objeto do Gerenciador de threads baseado na interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) chamando a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com um ponteiro para um objeto do Gerenciador de threads. Veja a seguir um exemplo de código de implementação de um objeto do Gerenciador de threads.
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  Ative o objeto Gerenciador de threads chamando o método [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) . Esse método fornece um ponteiro para um [identificador de cliente](tfclientid.md) usado para criar um objeto de contexto. O Gerenciador de threads é usado para implementar um objeto do Gerenciador de documentos.
3.  Crie um objeto do Gerenciador de documentos com base na interface [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) chamando o método [ITfThreadMgr:: CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) com um ponteiro para o objeto do Gerenciador de documentos. O objeto Gerenciador de documentos é usado para implementar um objeto de contexto que é o armazenamento de texto.
4.  Crie um objeto de contexto do Gerenciador de documentos chamando o método [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) com o ponteiro para o objeto de armazenamento de texto e um ponteiro para o identificador do cliente de ativar o Gerenciador de threads. Veja a seguir um exemplo de criação de um objeto de contexto:
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  Envie por push o objeto de contexto para a pilha com o método [ITfDocumentMgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) . Veja a seguir um exemplo de envio do objeto de contexto para a pilha:
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a>Como modificar o armazenamento de texto

O método **ITfDocumentMgr::P USH** chama **ITextStoreACP:: AdviseSink** com um ponteiro para a interface do coletor de aviso para instalar um novo coletor de aviso ou modificar um coletor de aviso existente. O coletor de aviso recebe notificações quando o armazenamento de texto é modificado por algo diferente do gerente, como entrada do usuário para o aplicativo. Os aplicativos devem chamar o método [ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) quando o método de entrada obtiver o foco. Outras notificações para o Gerenciador de thread são fornecidas chamando para os métodos de interface **ITextStoreACPSink** apropriados.

No entanto, os aplicativos não devem chamar os métodos de interface **ITextStoreACPSink** em resposta aos métodos de interface **ITextStoreACP** . Os aplicativos só devem chamar métodos de interface **ITextStoreACPSink** quando o armazenamento de texto é modificado por algo diferente do gerente.

O conteúdo do repositório de texto pode ser modificado com um estado de entrada temporário chamado de [composição](compositions.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Âncoras](ranges.md)
</dt> <dt>

[Composições](compositions.md)
</dt> <dt>

[Bloqueios de documentos](document-locks.md)
</dt> <dt>

[ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[ITfThreadMgrEventSink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[Acessibilidade Ativa da Microsoft](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 