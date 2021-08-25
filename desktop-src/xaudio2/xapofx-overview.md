---
description: XAPOFX é uma coleção de efeitos de áudio que implementam as interfaces XAPO para uso no XAudio2. XAPOFX contém vários efeitos e um mecanismo comum para criar instâncias de efeito.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Visão geral do XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae339a022ae5e2e880dcd130dbe055d0fde9cd28a95ea52c1238e2ade080ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005716"
---
# <a name="xapofx-overview"></a>Visão geral do XAPOFX

XAPOFX é uma coleção de efeitos de áudio que implementam as interfaces [XAPO](xapo-overview.md) para uso no XAudio2. XAPOFX contém vários efeitos e um mecanismo comum para criar instâncias de efeito.

## <a name="included-effects"></a>Efeitos incluídos

A tabela a seguir descreve os efeitos incluídos em XAPOFX. 

| Efeito             | Descrição                                                                                                                                                                                           | Estrutura de parâmetros                                                     | Constantes de parâmetro                                              | Requisitos                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Um efeito de eco.                                                                                                                                                                                       | [**PARÂMETROS FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Constantes FXECHO**](fxecho-constants.md)                     | Dá suporte apenas a formatos de áudio FLOAT32.                                                                                      |
| FXEQ               | Um equalizador de quatro bandas.                                                                                                                                                                                | [**PARÂMETROS FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Constantes FXEQ**](fxeq-constants.md)                         | Dá suporte apenas a formatos de áudio FLOAT32. A taxa de exemplo deve estar entre 22.000 Hz e 48.000 Hz.                             |
| FXMasteringLimiter | Um limitador de volume.                                                                                                                                                                                     | [**PARÂMETROS FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Constantes FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Dá suporte apenas a formatos de áudio FLOAT32.                                                                                      |
| FXReverb           | Um efeito reverb simples.<br/> O XAudio2 também fornece um efeito na implementação do Reverb Digital de NatAna que pode ser instanciado com [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**PARÂMETROS FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Constantes FXREVERB**](fxreverb-constants.md)                 | Dá suporte apenas a formatos de áudio FLOAT32. Além disso, ele só dá suporte à entrada mono para saída mono e entrada estéreo para saída estéreo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Criando uma instância de um efeito incluído em XAPOFX

O XAPOFX fornece a [**função CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) como um mecanismo comum para criar instâncias de efeito. **CreateFX** recebe a CLSID de um efeito e retorna um ponteiro de interface IUnknown para uma instância do efeito.

## <a name="using-xapofx-in-xaudio2"></a>Usando XAPOFX no XAudio2

Os efeitos instanados com [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) são usados no XAudio2 anexando-os às vozes. Cada voz XAudio2 tem uma cadeia de efeitos que contém zero ou mais efeitos de áudio. Os dados de áudio enviados a uma voz são passados por meio de cada efeito na cadeia antes que eles são enviados para os destinos de saída da voz. A voz assume a saída de cada efeito e a alimenta para o próximo efeito na cadeia até que nenhum efeito seja deixado na cadeia. Para anexar um efeito XAPOFX a uma voz XAudio2, preencha uma estrutura [**XAUDIO2 \_ EFFECT \_ CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com as informações do efeito e passe-a para [**IXAudio2Voice::SetEffectChain.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)

Para obter mais informações sobre cadeias de efeito XAudio2, consulte Efeitos de áudio [XAudio2](xaudio2-audio-effects.md).

Para ver um exemplo de como usar XAPOFX no XAudio2, consulte [Como usar XAPOFX no XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>Efeitos implícitos do XAudio2

Além da biblioteca de XAPOs fornecidas pelo XAPOFX, o XAudio2 tem efeitos de áudio de reverb e medidor de volume integrados. Você pode criar esses efeitos integrados com [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) e [**XAudio2CreateVolumeMeter.**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) Consulte [Como criar uma cadeia de efeitos](how-to--create-an-effect-chain.md) para ver um exemplo de como usar um desses efeitos integrados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> </dl>

 

 
