---
description: Criando o objeto Multiplexador
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Criando o objeto Multiplexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164208"
---
# <a name="creating-the-multiplexer-object"></a>Criando o objeto Multiplexador

O multiplexador de ASF é um objeto de camada WMContainer que funciona com o [objeto de dados ASF](asf-file-structure.md) e dá a um aplicativo a capacidade de gerar pacotes de dados ASF para fluxos de mídia.

O objeto multiplexador expõe a interface [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) . Para criar o multiplexador, chame [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer). Essa função retorna um ponteiro para um objeto vazio. Se o aplicativo estiver gravando um novo arquivo ASF, o aplicativo deverá inicializar o multiplexador com um objeto ContentInfo. Para fazer isso, chame [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize). O objeto ContentInfo especificado representa o objeto de cabeçalho ASF do novo arquivo. Para obter informações sobre como criar e inicializar o objeto ContentInfo para um novo arquivo, consulte [inicializando o objeto ContentInfo de um novo arquivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).

O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analisa o objeto ContentInfo para coletar informações de configuração de fluxo, como o número de fluxos, o tamanho do pacote, a preversão. Opcionalmente, o multiplexador também pode precisar de parâmetros de Bucket de vazamento e das unidades de extensão de carga. Essas informações são necessárias para gerar pacotes de dados que correspondam aos requisitos definidos no objeto de cabeçalho ASF. O método **Initialize** configura o multiplexador com base no tipo de mídia e nas definições de configuração dos fluxos. Por exemplo, se um fluxo estiver configurado para ter extensões de carga (consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md)) e, em seguida, o multiplexador será configurado para adicionar esses valores aos pacotes de dados gerados.

O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) também obtém um identificador para o objeto de dados inicial que foi criado durante a criação do objeto ContentInfo para gravação. Durante a geração de pacotes de dados, o multiplexador adiciona pacotes ao objeto de dados e os atualiza adequadamente. Depois que o multiplexador gera todos os pacotes de dados, ele atualiza o objeto ContentInfo fornecido para que determinados valores, como o número de pacotes de dados, sejam atualizados.

O exemplo de código a seguir mostra como criar um multiplexador e inicializá-lo com um objeto ContentInfo.


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



Para ver essa função usada em um aplicativo completo, consulte [tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a>Inicialização do Multiplexador e configurações de Bucket de vazamento

O método [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura o multiplexador para determinar o fluxo de dados do Bucket de vazamento. Para configurar esses parâmetros, verifique se os valores de propriedade a seguir estão definidos no objeto ContentInfo especificado. Para obter informações sobre como definir essas propriedades, consulte [definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).

-   [**MFPKEY \_ Propriedade de \_ \_ taxa de bits de ajuste**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) automático do ASFMEDIASINK: indica se o multiplexador precisa ajustar a taxa de bits automaticamente para manter o fluxo de dados no Bucket de vazamentos. Essa configuração pode ser alterada pelo aplicativo chamando [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) e passando o sinalizador de **taxa de \_ bits de \_ AutoAjuste \_ do Multiplexador MFASF** .

-   [**MFPKEY \_ Propriedade \_ \_ sendtime de base ASFMEDIASINK**](mfpkey-asfmediasink-base-sendtime-property.md) : a hora de envio indica quando a carga dentro do Bucket de vazamento será liberada. Os horários de envio devem ser iguais ou anteriores ao horário da apresentação, pois a carga deve ter tempo para chegar ao destino antes da hora da apresentação.

    Esse valor de propriedade é a primeira hora de envio. O multiplexador usa esse valor para calcular os tempos de envio subsequentes para garantir que os dados fluem pelo Bucket constantemente. Se o sinalizador de **taxa de bits do MFASF \_ multiplexador \_ AutoAjuste \_** tiver sido definido no Multiplexador, o multiplexador ajustará a taxa de bits para que a carga seja enviada quando a janela do buffer estiver perto de estar cheia. Se o sinalizador não estiver definido, o multiplexador falhará ao gerar pacotes de dados devido à saturação da largura de banda.

O multiplexador Obtém informações de configuração de fluxo do perfil ASF associado ao objeto ContentInfo especificado no método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) . As informações de configuração de fluxo incluem parâmetros de Bucket de vazamentos. Esse valor é exigido pelo multiplexador para gerar pacotes de dados.

Para especificar os parâmetros de Bucket de vazamento, defina os valores no atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) no objeto de configuração de fluxo que representa o fluxo no perfil. Para usar o valor da janela buffer, que é usado pelo codificador, chame [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md). O valor da janela de buffer real só é conhecido depois de definir o tipo de mídia de saída do codificador. Para obter informações sobre como definir o tipo de mídia de saída, consulte [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> Os valores de Bucket de vazamento usados pelo codificador podem ser diferentes no objeto ContentInfo que foi fornecido pelo perfil ASF que foi usado para criar o multiplexador.

 

O método [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) atualiza o objeto ContentInfo para que os valores corretos sejam refletidos no objeto de cabeçalho ASF final.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Multiplexador ASF](asf-multiplexer.md)
</dt> <dt>

[Gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
