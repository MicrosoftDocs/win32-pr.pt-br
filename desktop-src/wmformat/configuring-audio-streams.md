---
title: configurando Fluxos de áudio
description: configurando Fluxos de áudio
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- fluxos, configurando fluxos de áudio
- codecs, configurando fluxos de áudio
- fluxos de áudio, configurando
- codecs, formatos
- fluxos, interface IWMCodecInfo
- IWMCodecInfo, fluxos de áudio
- fluxos, sincronização A/V
- fluxos de áudio, sincronização A/V
- Sincronização de A/V
- fluxos, sincronizando A/V
- fluxos de áudio, sincronizando A/V
- fluxos, formatos de áudio de baixo atraso
- fluxos de áudio, formatos de áudio de baixo atraso
- codecs, formatos de áudio de baixo atraso
- fluxos, taxa de bits variável (VBR)
- fluxos de áudio, taxa de bits variável (VBR)
- codecs, taxa de bits variável (VBR)
- taxa de bits variável (VBR), configurando
- VBR (taxa de bits variável), configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28c32e9d0e237e72f693bded74c7620d33845261a6137afdf58b04f35f441f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548026"
---
# <a name="configuring-audio-streams"></a>configurando Fluxos de áudio

Fluxos de áudio geralmente são os mais simples de configurar. Obtenha uma configuração de fluxo do codec usando os métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) , conforme descrito em [obtendo informações de configuração de fluxo de codecs](getting-stream-configuration-information-from-codecs.md). Na maioria das circunstâncias, você não deve alterar as configurações das recuperadas.

O formato de codec que você seleciona entre os enumerados depende do uso pretendido dos arquivos ASF feitos com o perfil. A descrição do formato do codec recuperado por [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) resume as características do formato. Se seu aplicativo não exibir as descrições para escolher entre elas, você poderá chamar **QueryInterface** na interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) do formato de codec para obter a interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) . Em seguida, você pode recuperar a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) chamando [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Ao examinar a estrutura do **\_ \_ tipo de mídia do WM** e a estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) que aponta, você pode determinar as configurações do formato do codec e compará-las aos seus requisitos.

## <a name="getting-audio-formats-for-av-synchronization"></a>Obtendo formatos de áudio para sincronização A/V

o codec de áudio de mídia Windows e o codec de Professional de áudio de mídia Windows são compatíveis com formatos de arquivos somente de áudio e arquivos de áudio/vídeo. Os formatos somente de áudio são otimizados para arquivos que contêm apenas dados de áudio, enquanto os formatos de áudio/vídeo são otimizados para áudio que está em um arquivo com um fluxo de vídeo. Ao enumerar formatos de codec para esses codecs, os formatos de áudio/vídeo vêm após os formatos de somente áudio. Todas as descrições de formato de áudio/vídeo contêm a cadeia de caracteres "(A/V)". Você pode identificar os formatos criados para sincronização de áudio/vídeo programaticamente verificando o número de pacotes por segundo. Os formatos de sincronização têm 5 ou mais pacotes por segundo se a taxa de bits for maior ou igual a 32.000 bits por segundo. Formatos com taxas de bits inferiores a 32.000 bits por segundo podem ser usados com vídeo sincronizado se usarem 3 ou mais pacotes por segundo. O exemplo de código no tópico [para localizar formatos de áudio](to-find-audio-formats.md) contém o código necessário para fazer essa verificação:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Obtendo Low-Delay formatos de áudio

o codec Windows media 9,1 e o codec Windows media Audio 9,1 Professional dão suporte a formatos de atraso baixo. Esses formatos têm uma janela de buffer menor do que outros formatos de áudio. O áudio de baixo atraso destina-se a melhorar o desempenho em cenários em que os arquivos ou fluxos serão alternados com frequência; por exemplo, um aplicativo que lista um número de músicas para streaming na interface do usuário e permite que os usuários alternem arbitrariamente entre elas.

Os formatos de atraso baixo estão disponíveis somente no modo CBR (One-Pass ou Two-pass). Todas as descrições de formato de atraso baixo contêm a cadeia de caracteres "atraso baixo". Você pode identificar os formatos programaticamente verificando o valor de taxa de bits do formato. Os formatos de atraso baixo são taxas de bits atribuídas que são 1 quilobits menores que as taxas de bits do formato normal equivalente. por exemplo, o codec Windows Media Audio 9,1 dá suporte a um formato CBR de passagem única com uma taxa de bits de 192 kbps. O formato de baixa demora equivalente tem uma taxa de bits de 191 kbps. além disso, com exceção do formato mono de 5 kbps com suporte pelo codec Windows Media Audio 9,1, os formatos de atraso baixo são os únicos formatos que têm um valor de taxa de bits ímpar.

## <a name="configuring-variable-bit-rate-audio"></a>Configurando áudio de taxa de bits variável

quando você precisa de um formato de taxa de bits variável (VBR) para um dos codecs de áudio de mídia Windows, você pode obtê-lo definindo as configurações de enumeração no método [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) . Defina g \_ wszVBREnabled como true e defina g \_ wszNumPasses como 1 para VBR com base em qualidade ou 2 para VBR de duas passagens (restrita ou irrestrita). se você estiver usando uma taxa de bits de passagem dupla restrita, será necessário definir manualmente a janela de taxa e buffer máximo para o fluxo usando os métodos de [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) , conforme descrito em [configurando a VBR Fluxos](configuring-vbr-streams.md).

Em perfis de VBR com base em qualidade, o membro **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** contém o nível de qualidade (de 1 a 100) no byte de ordem inferior e os três bytes de ordem superior são definidos como 0x7fffff. Não tente modificar a configuração de qualidade modificando esse valor manualmente; Você deve usar o formato conforme ele é recuperado do codec. Para usar um valor de qualidade diferente, você deve enumerar formatos até encontrar um que atenda às suas necessidades. Além disso, o **nAvgBytesPerSec** não será preservado no arquivo ASF; Quando você obtém a estrutura **WAVEFORMATEX** para um arquivo que foi aberto com o objeto leitor, **nAvgBytesPerSec** contém um valor aproximado que representa o número médio de bytes por segundo.

> [!Note]  
> Ao configurar fluxos de áudio, você nunca deve ter um valor de janela de buffer de áudio maior que o valor de fluxos de vídeo no arquivo. Normalmente, isso não é um problema, pois os valores de janela do buffer de áudio devem variar entre 1,5 e 3 segundos e os valores de vídeo devem variar entre 3 e 5 segundos. Se uma janela de buffer de áudio for maior que uma janela de buffer de vídeo, o arquivo será reproduzido com os fluxos um pouco fora de sincronização.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**Para localizar formatos de áudio**](to-find-audio-formats.md)
</dt> </dl>

 

 