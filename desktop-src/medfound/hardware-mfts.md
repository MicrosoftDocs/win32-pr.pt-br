---
description: Este tópico descreve como escrever uma transformação Media Foundation (MFT) que atua como um proxy para um codificador de hardware, decodificador ou DSP (processador de sinal digital).
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: Hardware MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532fef959e2c2b5946d5a27ad98106a2e25cc77f8426c0a871e821c7298a69f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724920"
---
# <a name="hardware-mfts"></a>Hardware MFTs

> [!Note]  
> Este tópico se aplica ao Windows 7 ou posterior.

 

Este tópico descreve como escrever uma transformação Media Foundation (MFT) que atua como um proxy para um codificador de hardware, decodificador ou DSP (processador de sinal digital).

> [!IMPORTANT]
> Se um codec de hardware usar o driver de classe multimídia AVStream, ele não exigirá um MFT personalizado. Media Foundation fornece um proxy AVStream para essa finalidade. As informações neste tópico se aplica somente no caso especial em que o codec de hardware não usa AVStream. Para obter mais informações, consulte [Suporte a codec de hardware no AVStream.](https://msdn.microsoft.com/library/dd568169.aspx)

 

Este tópico contém as seguintes seções:

-   [Introdução](#introduction)
-   [Atributos MFT de hardware](#hardware-mft-attributes)
-   [Sequência de handshake de hardware](#hardware-handshake-sequence)
-   [Processamento de dados](#data-processing)
-   [Decodificador/Codificador emparelhado](#paired-decoderencoder)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Qualquer codec de hardware que não se baseia no AVStream deve fornecer seu próprio MFT para atuar como um proxy para o driver. Um codec de hardware pode incorporar vários blocos funcionais distintos:

-   Codificador
-   Decodificador
-   Conversão de dimensionamento/formato de quadro

Cada uma dessas funções deve ser gerenciada por um MFT separado. Um MFT de hardware nunca deve atuar como um "transcodificador" de várias finalidades. Em vez disso, coloque funções de codificação em um MFT codificador e decodificar funções em um MFT decodificador. Se o hardware oferecer conversões de formato e dimensionamento de quadros, coloque essas funções em um processador de vídeo separado, registrado na categoria PROCESSADOR DE VÍDEO de CATEGORIA **MFT. \_ \_ \_** Se o hardware não dá suporte ao dimensionamento de quadros ou à conversão de formato, Media Foundation fornece um processador de vídeo de software.

Os MFTs de hardware têm os seguintes requisitos gerais:

-   Os MFTs de hardware devem usar o novo modelo de processamento assíncrono, conforme descrito em [MFTs assíncronos.](asynchronous-mfts.md)
-   Os MFTs de hardware devem dar suporte a alterações de formato dinâmico, conforme descrito em [Alterações de formato dinâmico.](basic-mft-processing-model.md)

## <a name="hardware-mft-attributes"></a>Atributos MFT de hardware

Um MFT de hardware deve implementar os seguintes métodos relacionados a atributos:

-   [**IMFTransform::GetAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)retorna um armazenamento de atributos para atributos MFT globais.
-   [**IMFTransform::GetInputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)retorna um armazenamento de atributos para um fluxo de entrada.
-   [**IMFTransform::GetOutputStreamAttributes:**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)retorna um armazenamento de atributos para um fluxo de saída.

Quando o MFT é criado pela primeira vez, ele deve definir os seguintes atributos em seu próprio armazenamento de atributos global (ou seja, o armazenamento de atributos retornado por [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)):



| Atributo                                                                                    | Descrição                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                               | Deve ser definido como **TRUE.** Indica que o MFT executa o processamento assíncrono.                                                                                                      |
| [Atributo de \_ URL de HARDWARE MFT ENUM \_ \_ \_](mft-enum-hardware-url-attribute.md)                   | Contém o link simbólico para o dispositivo de hardware.<br/> O carregador de topologia usa a presença desse atributo para testar se um MFT representa um dispositivo de hardware.<br/> |
| [**ALTERAÇÃO DE FORMATO \_ DINÂMICO DE SUPORTE \_ \_ DO \_ MFT**](mft-support-dynamic-format-change-attribute.md) | Deve ser definido como **TRUE.** Indica que o MFT dá suporte a alterações de formato dinâmico.                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>Sequência de handshake de hardware

Se dois MFTs representarem o mesmo dispositivo físico, eles poderão trocar dados dentro do hardware, por exemplo, por um barramento de hardware. Não é necessário copiar os dados para a memória do sistema e, em seguida, de volta para o dispositivo.

No diagrama a seguir, os MFTs rotulados como "A" e "B" representam blocos funcionais dentro do mesmo hardware. Por exemplo, em um cenário de transcodificação, "A" pode representar um decodificador de hardware e "B" pode representar um codificador de hardware. O fluxo de dados entre "A" e "B" ocorre dentro do hardware. O MFT rotulado como "C" é um MFT de software. O fluxo de dados de "B" para "C" usa a memória do sistema.

![diagrama mostrando caixas rotuladas como a a c e um codec de hardware: um aponta para b e o codec, o codec aponta para b e b aponta para c](images/proxy-mft.png)

Para estabelecer uma conexão de hardware, os dois MFTs de hardware devem usar um canal de comunicação privado. Essa conexão é estabelecida durante a negociação de formato, antes que os tipos de mídia sejam definidos e antes da primeira chamada para [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) O processo de conexão funciona da seguinte forma:

1.  O carregador de topologia verifica os dois MFTs quanto à presença do atributo atributo de [ \_ URL de \_ \_ \_ HARDWARE ENUM MFT.](mft-enum-hardware-url-attribute.md) Observe que ele não examina o valor desse atributo.
2.  Se [o Atributo de URL de \_ \_ \_ \_ HARDWARE MFT ENUM](mft-enum-hardware-url-attribute.md) estiver presente em ambos os MFTs, o carregador de topologia faz o seguinte:
    1.  O carregador de topologia chama [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) no MFT (A) upstream. Esse método retorna um [**ponteiro IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Deixe esse ponteiro ser anotado *como pUpstream.*
    2.  O carregador de topologia chama [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) no MFT downstream (B). Essa chamada também retorna um [**ponteiro IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Deixe que esse ponteiro seja anotado *como pDownstream.*
    3.  O carregador de topologia define o atributo [MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE](mft-connected-stream-attribute.md) em *pDownstream* chamando [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). O valor do atributo é o *ponteiro pUpstream.*
    4.  O carregador de topologia define o [atributo MFT \_ CONNECTED TO \_ \_ HW \_ STREAM](mft-connected-to-hw-stream.md) como **TRUE** em *pDownstream e* *pUpstream.*
3.  Neste ponto, o MFT downstream tem um ponteiro para o armazenamento de atributos do MFT upstream, conforme mostrado no diagrama a seguir.

    ![diagrama com cada mfts apontando para seu fluxo, cada fluxo apontando para seu armazenamento e o armazenamento de entrada com uma linha tracejada para o armazenamento de saída](images/proxy-mft2.png)

    > [!Note]  
    > Para maior clareza, esse diagrama mostra os fluxos e os armazenamentos de atributo como objetos distintos, mas isso não é necessário para a implementação.

     

4.  O MFT downstream usa o ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para estabelecer um canal de comunicação privado com o MFT upstream. Como o canal é privado, o mecanismo exato é definido pela implementação. Por exemplo, o MFT pode consultar uma interface COM privada.

Durante a etapa 4, o MFT downstream deve verificar se os dois MFTs compartilham o mesmo dispositivo físico. Caso não, eles deverão voltar a usar a memória do sistema para o transporte de dados. Isso permite que o MFT opere corretamente com MFTs de software e outros dispositivos de hardware.

Se o handshake for bem-sucedido e os dois MFTs compartilharem um canal de dados privado, eles não usarão o modelo de processamento de dados padrão (descrito na próxima seção) no ponto de conexão. Especificamente, o MFT downstream não envia [eventos METransformNeedInput;](metransformneedinput.md) Para obter mais detalhes, consulte a próxima seção neste tópico.

## <a name="data-processing"></a>Processamento de dados

Quando um MFT de hardware usa memória do sistema para transporte de dados, o processo funciona da seguinte forma:

1.  Para solicitar mais entrada, o MFT envia um [evento METransformNeedInput.](metransformneedinput.md)
2.  O [evento METransformNeedInput](metransformneedinput.md) faz com que o pipeline chame [**IMFTransform::P rocessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
3.  Quando o MFT tem dados de saída, o MFT envia [um evento METransformHaveOutput.](metransformhaveoutput.md)
4.  O [evento METransformHaveOutput](metransformhaveoutput.md) faz com que o pipeline chame [**IMFTransform::P rocessOutput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)

Para obter detalhes, consulte [MFTs assíncronos.](asynchronous-mfts.md)

No entanto, se o MFT usar um canal de hardware, ele não enviará esses eventos no ponto de conexão de hardware, pois toda a transferência de dados ocorre internamente dentro do hardware. Portanto, o pipeline não chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ou [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no ponto de conexão.

Por exemplo, considere o primeiro diagrama neste tópico. Dada essa configuração, o processamento de dados ocorreria da seguinte forma:

1.  "A" envia [METransformNeedInput para](metransformneedinput.md) solicitar dados.
2.  O pipeline chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) em "A".
3.  "A" e "B" processam os dados em hardware.
4.  Quando o processamento for concluído, "B" enviará um [evento METransformHaveOutput.](metransformhaveoutput.md)
5.  O pipeline chama [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) em "B".

## <a name="paired-decoderencoder"></a>Decodificador/Codificador emparelhado

Se um decodificador e um codificador estão localizados no mesmo chip de hardware, pode ser preferível usá-los juntos ao transcodificar. Ou seja, selecionar um deve fazer com que o outro seja selecionado no pipeline de transcodificação. Para garantir que os codecs de hardware correspondentes sejam escolhidos, os dois MFTs de codec devem oferecer um tipo de mídia personalizado. Para criar um tipo de mídia personalizado:

-   De definir o [**atributo \_ MF MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) como **Áudio MFMediaType \_ ou** **Vídeo MFMediaType, \_** conforme apropriado.
-   De definir o [**atributo \_ MF MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) como um valor guid personalizado.

Outros atributos de tipo são opcionais. O decodificador retorna o tipo personalizado de [**seu IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)e o codificador retorna o tipo personalizado de seu [**método IMFTransform::GetInputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) Em ambos os casos, o tipo personalizado deve ser a primeira entrada na lista (*dwTypeIndex* = 0).

Para trabalhar com codecs de software, o codec também deve retornar pelo menos um formato padrão, como NV12 para vídeo. Os formatos padrão devem aparecer após o tipo personalizado (*dwTypeIndex* > 0). Se os dois codecs sempre devem ser emparelhados e não podem interoperar com codecs de software, os MFTs devem retornar apenas o formato personalizado e não retornar nenhum formato padrão.

> [!Note]  
> Se um decodificador não retornar nenhum formato padrão, ele não poderá ser usado para reprodução com o [Renderização de Vídeo Aprimorado.](enhanced-video-renderer.md) Nesse caso, ele deve ser registrado como um decodificador somente transcodificador. Consulte [Decodificadores somente transcodificadores](implementing-a-codec-mft.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um MFT personalizado](writing-a-custom-mft.md)
</dt> <dt>

[Implementando um Codec MFT](implementing-a-codec-mft.md)
</dt> <dt>

[Media Foundation transformação](media-foundation-transforms.md)
</dt> </dl>

 

 




