---
title: Configurando o Fluxos
description: Configurando o Fluxos
ms.assetid: 6ddd9bc1-3fde-4098-afce-fdda461ced62
keywords:
- fluxos, configurando fluxos de áudio
- codecs, configurando fluxos de áudio
- fluxos de áudio, configurando
- codecs,formats
- streams, interface IWMCodecInfo
- IWMCodecInfo, fluxos de áudio
- streams, sincronização A/V
- fluxos de áudio, sincronização A/V
- Sincronização A/V
- streams, sincronizando A/V
- fluxos de áudio, sincronizando A/V
- fluxos, formatos de áudio de baixo atraso
- fluxos de áudio, formatos de áudio de baixo atraso
- codecs, formatos de áudio de baixo atraso
- streams, taxa de bits variável (VBR)
- fluxos de áudio, taxa de bits variável (VBR)
- codecs, taxa de bits variável (VBR)
- VBR (taxa de bits variável), configurando
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
# <a name="configuring-audio-streams"></a>Configurando o Fluxos

Os fluxos de áudio geralmente são os mais simples de configurar. Obter uma configuração de fluxo do codec usando os métodos [**de IWMCodecInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) conforme descrito em Obter informações de configuração de fluxo [de codecs](getting-stream-configuration-information-from-codecs.md). Na maioria das circunstâncias, você não deve alterar as configurações das recuperadas.

O formato de codec selecionado entre os enumerados depende do uso pretendido dos arquivos ASF feitos com o perfil. A descrição do formato codec recuperada por [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) resume as características do formato. Se seu aplicativo não exibir as descrições para escolher entre elas, você poderá chamar **QueryInterface** na interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) do formato codec para obter a interface [**IWMMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) Em seguida, você pode recuperar [**a estrutura WM MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) chamando [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Examinando a estrutura **WM \_ MEDIA \_ TYPE** e a estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) para a qual ela aponta, você pode determinar as configurações do formato codec e compará-las às suas necessidades.

## <a name="getting-audio-formats-for-av-synchronization"></a>Obter formatos de áudio para sincronização A/V

O codec Windows Media Audio e o codec Windows Media Audio Professional suporte a formatos para arquivos somente áudio e para arquivos de áudio/vídeo. Os formatos somente áudio são otimizados para arquivos que contêm apenas dados de áudio, enquanto os formatos de áudio/vídeo são otimizados para áudio que está em um arquivo com um fluxo de vídeo. Ao enumerar formatos de codec para esses codecs, os formatos de áudio/vídeo vêm após os formatos somente áudio. Todas as descrições de formato de áudio/vídeo contêm a cadeia de caracteres "(A/V)". Você pode identificar os formatos projetados para sincronização de áudio/vídeo programaticamente verificando o número de pacotes por segundo. Os formatos de sincronização terão 5 ou mais pacotes por segundo se a taxa de bits for maior ou igual a 32.000 bits por segundo. Formatos com taxas de bits menores que 32.000 bits por segundo poderão ser usados com vídeo sincronizado se usarem três ou mais pacotes por segundo. O exemplo de código no [tópico Para Encontrar Formatos de](to-find-audio-formats.md) Áudio contém o código necessário para fazer essa verificação:


```C++
if((pWave->nAvgBytesPerSec / pWave->nBlockAlign) >= 
       ((pWave->nAvgBytesPerSec >= 4000) ? 5.0 : 3.0))
{
    // Set this stream configuration as the new best match.
}
```



## <a name="getting-low-delay-audio-formats"></a>Obter Low-Delay de áudio

O codec Windows Media 9.1 e o codec Windows Media Audio 9.1 Professional codec têm suporte para formatos de baixo atraso. Esses formatos têm uma janela de buffer menor do que outros formatos de áudio. Áudio de baixo atraso destina-se a melhorar o desempenho em cenários em que arquivos ou fluxos serão alternados com frequência; por exemplo, um aplicativo que lista várias músicas para streaming na interface do usuário e permite que os usuários alternem arbitrariamente entre eles.

Formatos de atraso baixo estão disponíveis somente no modo CBR (uma passagem ou duas passões). Todas as descrições de formato de atraso baixo contêm a cadeia de caracteres "Atraso Baixo". Você pode identificar os formatos programaticamente verificando o valor da taxa de bits do formato. Os formatos de atraso baixo são taxas de bits atribuídas que são 1 quilobit menor que as taxas de bits do formato normal equivalente. Por exemplo, o codec Windows Media Audio 9.1 dá suporte a um formato CBR de passagem única com uma taxa de bits de 192 kbps. O formato de atraso baixo equivalente tem uma taxa de bits de 191 kbps. Além disso, com exceção do formato mono de 5 kbps com suporte do codec Windows Media Audio 9.1, os formatos de atraso baixo são os únicos formatos que têm um valor de taxa de bits ímpar.

## <a name="configuring-variable-bit-rate-audio"></a>Configurando áudio de taxa de bits variável

Quando você precisa de um formato de VBR (taxa de bits variável) para um dos codecs de áudio de mídia do Windows, você pode obter isso definindo as configurações de enumeração no método [**IWMCodecInfo3::SetCodecEnumerationSetting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) De definir g \_ wszVBREnabled como True e de definir g wszNumPasses como 1 para VBR baseado em qualidade ou 2 para VBR de duas passagens (restrito ou irr \_ pouco restrito). Se você estiver usando uma VBR de duas passs restrita, deverá definir manualmente a taxa máxima de bits e a janela de buffer para o fluxo usando os métodos [**de IWMPropertyVault,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) conforme descrito em Configurando o [VBR Fluxos](configuring-vbr-streams.md).

Em perfis VBR baseados em qualidade, o membro **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** contém o nível de qualidade (1 a 100) no byte de ordem baixa e os três bytes de ordem alta são definidos como 0x7fffff. Não tente modificar a configuração de qualidade modificando esse valor manualmente; você deve usar o formato conforme ele é recuperado do codec. Para usar um valor de qualidade diferente, você deve enumerar formatos até encontrar um que atenda às suas necessidades. Além disso, **nAvgBytesPerSec** não será preservado no arquivo ASF; quando você obtém a estrutura **WAVEFORMATEX** para um arquivo que foi aberto com o objeto de leitor, **nAvgBytesPerSec** contém um valor aproximado que representa o número médio de bytes por segundo.

> [!Note]  
> Ao configurar fluxos de áudio, você nunca deve ter um valor de janela de buffer de áudio maior que o valor de qualquer fluxo de vídeo no arquivo. Normalmente, isso não é um problema, pois os valores da janela do buffer de áudio devem variar entre 1,5 e 3 segundos e os valores de vídeo devem variar entre 3 e 5 segundos. Se uma janela de buffer de áudio for maior que uma janela de buffer de vídeo, o arquivo reproduzirá com os fluxos ligeiramente fora de sincronização.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando Fluxos**](configuring-streams.md)
</dt> <dt>

[**Para encontrar formatos de áudio**](to-find-audio-formats.md)
</dt> </dl>

 

 