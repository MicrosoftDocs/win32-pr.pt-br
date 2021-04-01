---
description: Este tópico descreve como gravar uma MFT (Media Foundation transformação) que atua como um proxy para um codificador de hardware, decodificador ou DSP (processador de sinal digital).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: MFTs de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164843"
---
# <a name="hardware-mfts"></a>MFTs de hardware

> [!Note]  
> Este tópico aplica-se ao Windows 7 ou posterior.

 

Este tópico descreve como gravar uma MFT (Media Foundation transformação) que atua como um proxy para um codificador de hardware, decodificador ou DSP (processador de sinal digital).

> [!IMPORTANT]
> Se um codec de hardware usar o driver de classe multimídia AVStream, ele não exigirá uma MFT personalizada. Media Foundation fornece um proxy AVStream para essa finalidade. As informações neste tópico aplicam-se somente ao caso especial em que o codec de hardware não usa AVStream. Para obter mais informações, consulte [hardware codec support in AVStream](https://msdn.microsoft.com/library/dd568169.aspx).

 

Este tópico contém as seguintes seções:

-   [Introdução](#introduction)
-   [Atributos de MFT de hardware](#hardware-mft-attributes)
-   [Sequência de handshake de hardware](#hardware-handshake-sequence)
-   [Processamento de dados](#data-processing)
-   [Decodificador/codificador emparelhado](#paired-decoderencoder)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Qualquer codec de hardware que não esteja baseado em AVStream deve fornecer seu próprio MFT para atuar como um proxy para o driver. Um codec de hardware pode incorporar vários blocos funcionais distintos:

-   Codificador
-   Decodificador
-   Escala de quadros/conversão de formato

Cada uma dessas funções deve ser gerenciada por um MFT separado. Um MFT de hardware nunca deve atuar como um "transcodificador" multipropósito. Em vez disso, coloque funções de codificação em um MFT do codificador e decodifique funções em um MFT do decodificador. Se o hardware oferecer conversões de formato e dimensionamento de quadros, coloque essas funções em um processador de vídeo separado, registrado na categoria MFT, na categoria do **\_ \_ \_ processador de vídeo** . Se o hardware não oferecer suporte à escala de quadros ou à conversão de formato, Media Foundation fornecerá um processador de vídeo de software.

Os MFTs de hardware têm os seguintes requisitos gerais:

-   Os MFTs de hardware devem usar o novo modelo de processamento assíncrono, conforme descrito em [MFTs assíncrona](asynchronous-mfts.md).
-   O hardware MFTs deve dar suporte a alterações de formato dinâmico, conforme descrito em [alterações de formato dinâmico](basic-mft-processing-model.md).

## <a name="hardware-mft-attributes"></a>Atributos de MFT de hardware

Um MFT de hardware deve implementar os seguintes métodos relacionados a atributos:

-   [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes): retorna um repositório de atributos para atributos MFT globais.
-   [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes): retorna um repositório de atributos para um fluxo de entrada.
-   [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes): retorna um repositório de atributos para um fluxo de saída.

Quando o MFT é criado pela primeira vez, ele deve definir os seguintes atributos em seu próprio repositório de atributo global (ou seja, o repositório de atributos retornado por [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):



| Atributo                                                                                    | Descrição                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transformação do MF em \_ \_ Async](mf-transform-async.md)                                               | Deve ser definido como **true**. Indica que o MFT executa o processamento assíncrono.                                                                                                      |
| [\_Atributo de \_ URL de hardware de enumeração de MFT \_ \_](mft-enum-hardware-url-attribute.md)                   | Contém o link simbólico para o dispositivo de hardware.<br/> O carregador de topologia usa a presença desse atributo para testar se um MFT representa um dispositivo de hardware.<br/> |
| [**o MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_**](mft-support-dynamic-format-change-attribute.md) | Deve ser definido como **true**. Indica que o MFT dá suporte a alterações de formato dinâmico.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Sequência de handshake de hardware

Se dois MFTs representam o mesmo dispositivo físico, eles podem trocar dados no hardware — por exemplo, em um barramento de hardware. Não é necessário copiar os dados na memória do sistema e, em seguida, voltar para o dispositivo.

No diagrama a seguir, o MFTs rotulado como "A" e "B" representam blocos funcionais dentro do mesmo hardware. Por exemplo, em um cenário de transcodificação, "A" pode representar um decodificador de hardware e "B" pode representar um codificador de hardware. O fluxo de dados entre "A" e "B" ocorre no hardware. O MFT rotulado como "C" é um MFT de software. O fluxo de dados de "B" para "C" usa a memória do sistema.

![diagrama mostrando caixas rotuladas a por c e um codec de hardware: um aponta para b e o codec, o codec aponta para b e b aponta para c](images/proxy-mft.png)

Para estabelecer uma conexão de hardware, os dois MFTs de hardware devem usar um canal de comunicação privada. Essa conexão é estabelecida durante a negociação de formato, antes que os tipos de mídia sejam definidos e antes da primeira chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). O processo de conexão funciona da seguinte maneira:

1.  O carregador de topologia verifica ambos os MFTs para a presença do atributo de [atributo de URL de hardware de enumeração de MFT \_ \_ \_ \_ ](mft-enum-hardware-url-attribute.md) . Observe que ele não examina o valor desse atributo.
2.  Se [o \_ \_ atributo de \_ URL \_ de hardware de enumeração de MFT](mft-enum-hardware-url-attribute.md) estiver presente em ambos os MFTs, o carregador de topologia fará o seguinte:
    1.  O carregador de topologia chama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) no MFT upstream (A). Esse método retorna um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Deixe que esse ponteiro seja denotado *pUpstream*.
    2.  O carregador de topologia chama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) no MFT downstream (B). Essa chamada também retorna um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Deixe que esse ponteiro seja denotado *pDownstream*.
    3.  O carregador de topologia define o atributo de [atributo de fluxo do MFT \_ \_ \_ conectado](mft-connected-stream-attribute.md) em *PDownstream* chamando [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). O valor do atributo é o ponteiro *pUpstream* .
    4.  O carregador de topologia define [a MFT \_ conectada ao atributo de \_ \_ \_ fluxo de HW](mft-connected-to-hw-stream.md) como **true** em *pDownstream* e *pUpstream*.
3.  Neste ponto, o MFT downstream tem um ponteiro para o armazenamento de atributos do MFT upstream, conforme mostrado no diagrama a seguir.

    ![diagrama com cada MFTs apontando para seu fluxo, cada fluxo apontando para seu armazenamento e o armazenamento de entrada com uma linha tracejada para o repositório de saída](images/proxy-mft2.png)

    > [!Note]  
    > Para maior clareza, esse diagrama mostra os fluxos e os repositórios de atributos como objetos distintos, mas isso não é necessário para a implementação.

     

4.  O MFT downstream usa o ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para estabelecer um canal de comunicação privada com o MFT upstream. Como o canal é privado, o mecanismo exato é definido pela implementação. Por exemplo, o MFT pode consultar uma interface COM privada.

Durante a etapa 4, o MFT downstream deve verificar se os dois MFTs compartilham o mesmo dispositivo físico. Caso contrário, eles deverão fazer fallback para usar a memória do sistema para o transporte de dados. Isso permite que o MFT opere corretamente com MFTs de software e outros dispositivos de hardware.

Se o handshake for bem sucedido e os dois MFTs compartilharem um canal de dados privado, eles não usarão o modelo de processamento de dados padrão (descrito na próxima seção) no ponto de conexão. Especificamente, o MFT downstream não envia eventos [METransformNeedInput](metransformneedinput.md) ; para obter mais detalhes, consulte a próxima seção neste tópico.

## <a name="data-processing"></a>Processamento de dados

Quando um MFT de hardware usa a memória do sistema para o transporte de dados, o processo funciona da seguinte maneira:

1.  Para solicitar mais entrada, o MFT envia um evento [METransformNeedInput](metransformneedinput.md) .
2.  O evento [METransformNeedInput](metransformneedinput.md) faz com que o pipeline chame [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
3.  Quando o MFT tem dados de saída, o MFT envia um evento [METransformHaveOutput](metransformhaveoutput.md) .
4.  O evento [METransformHaveOutput](metransformhaveoutput.md) faz com que o pipeline chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Para obter detalhes, consulte [MFTs assíncrono](asynchronous-mfts.md).

No entanto, se o MFT usar um canal de hardware, ele não enviará esses eventos no ponto de conexão de hardware, pois toda a transferência de dados ocorre internamente no hardware. Portanto, o pipeline não chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ou [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no ponto de conexão.

Por exemplo, considere o primeiro diagrama neste tópico. Dada essa configuração, o processamento de dados ocorrerá da seguinte maneira:

1.  "A" envia [METransformNeedInput](metransformneedinput.md) para dados de solicitação.
2.  O pipeline chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) em "A".
3.  "A" e "B" processam os dados no hardware.
4.  Quando o processamento for concluído, "B" enviará um evento [METransformHaveOutput](metransformhaveoutput.md) .
5.  O pipeline chama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) em "B".

## <a name="paired-decoderencoder"></a>Decodificador/codificador emparelhado

Se um decodificador e um codificador estiverem localizados no mesmo chip de hardware, poderá ser preferível usá-los juntos ao transcodificar. Ou seja, a seleção de uma deve fazer com que a outra seja selecionada no pipeline de transcodificação. Para garantir que os codecs de hardware correspondentes sejam escolhidos, o codec MFTs deve oferecer um tipo de mídia personalizado. Para criar um tipo de mídia personalizado:

-   Defina o atributo de [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) como **MFMediaType \_ Audio** ou **MFMediaType \_ Video**, conforme apropriado.
-   Defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) como um valor de GUID personalizado.

Outros atributos de tipo são opcionais. O decodificador retorna o tipo personalizado de seu [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), e o codificador retorna o tipo personalizado do seu método [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) . Em ambos os casos, o tipo personalizado deve ser a primeira entrada na lista (*dwTypeIndex* = 0).

Para trabalhar com codecs de software, o codec também deve retornar pelo menos um formato padrão, como NV12 para vídeo. Os formatos padrão devem aparecer após o tipo personalizado (*dwTypeIndex* > 0). Se os dois codecs precisarem ser sempre emparelhados e não puderem interoperar com os codecs de software, o MFTs deverá retornar apenas o formato personalizado e não retornar nenhum formato padrão.

> [!Note]  
> Se um decodificador não retornar nenhum formato padrão, ele não poderá ser usado para reprodução com o [processador de vídeo aprimorado](enhanced-video-renderer.md). Nesse caso, ele deve ser registrado como um decodificador somente de transcodificação. Consulte [decodificadores somente de transcodificação](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> <dt>

[Implementando uma MFT do codec](implementing-a-codec-mft.md)
</dt> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




