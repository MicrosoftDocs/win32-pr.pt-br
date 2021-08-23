---
description: A API XAPO fornece a interface IXAPO e a classe CXAPOBase para a criação de novos tipos XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Como: Criar um XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea17729c5a6d872d98443c85f79dc72e8eee6dd2233b99f31e189a9eb28708e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583846"
---
# <a name="how-to-create-an-xapo"></a>Como: Criar um XAPO

A API XAPO fornece a interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e a classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para a criação de novos tipos XAPO. A interface **IXAPO** contém todos os métodos que precisam ser implementados para criar um novo XAPO. A classe **CXAPOBase** fornece uma implementação básica da interface **IXAPO** . **CXAPOBase** implementa todos os métodos de interface **IXAPO** , exceto o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que é exclusivo para cada XAPO.

## <a name="to-create-a-new-static-xapo"></a>Para criar um novo XAPO estático

1.  Derive uma nova classe XAPO da classe base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .

    > [!Note]  
    > XAPOs implemente a interface **IUnknown** . As interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluem os três métodos **IUnknown** : **QueryInterface**, **AddRef** e **Release**. O [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornece implementações de todos os três métodos **IUnknown** . Uma nova instância de **CXAPOBase** terá uma contagem de referência de 1. Ele será destruído quando sua contagem de referência se tornar 0. Para permitir que o XAudio2 destrua uma instância de um XAPO quando ele não for mais necessário, chame **IUnknown:: Release** no XAPO depois que ele for adicionado a uma cadeia de efeito XAudio2. Consulte [como: usar um XAPO no XAudio2](how-to--use-an-xapo-in-xaudio2.md) para obter mais informações sobre como usar um XAPO com XAudio2.

     

2.  Substitua a implementação da classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) do método [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .

    A substituição de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permite que informações sobre o formato dos dados de áudio sejam armazenados para uso em [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process).

3.  Implemente o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .

    XAudio2 chama o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) sempre que um XAPO precisa processar dados de áudio. O **processo** contém a massa do código para um XAPO.

## <a name="implementing-the-process-method"></a>Implementando o método Process

O método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) aceita buffers de fluxo para dados de áudio de entrada e saída. Um XAPO típico esperará um buffer de fluxo de entrada e um buffer de fluxo de saída. Você deve basear o processamento de dados do buffer de fluxo de entrada no formato especificado na função [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e quaisquer sinalizadores passados para a função **process** com o buffer de fluxo de entrada. Copie os dados de buffer de fluxo de entrada processados para o buffer de fluxo de saída. Defina o parâmetro BufferFlags do buffer de fluxo de saída como o [**\_ buffer XAPO \_ válido**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) ou o **buffer XAPO é \_ \_ silencioso**.

O exemplo a seguir demonstra uma implementação de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e de [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que simplesmente copia dados de um buffer de entrada para um buffer de saída. No entanto, não haverá processamento se o buffer de entrada estiver marcado com o [**\_ buffer XAPO \_ silencioso**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



Ao escrever um método de [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , é importante observar que os dados de áudio XAudio2 são intercalados. Isso significa que os dados de cada canal são adjacentes a um número de exemplo específico. Por exemplo, se houver uma onda de 4 canais tocando em uma voz de origem XAudio2, os dados de áudio serão uma amostra do canal 0, uma amostra do canal 1, uma amostra do canal 2, uma amostra do canal 3 e, em seguida, a próxima amostra dos canais 0, 1, 2, 3 e assim por diante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Visão geral do XAPO](xapo-overview.md)
</dt> </dl>

 

 
