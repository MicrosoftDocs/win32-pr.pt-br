---
description: XAPOFX é uma coleção de efeitos de áudio que implementam as interfaces XAPO para uso no XAudio2. XAPOFX contém vários efeitos e um mecanismo comum para a criação de instâncias de efeito.
ms.assetid: 762062de-4e19-5e42-8059-e2f8741bd362
title: Visão geral do XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8979b5de50406d46bc472e18ca4a6479679e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501929"
---
# <a name="xapofx-overview"></a>Visão geral do XAPOFX

XAPOFX é uma coleção de efeitos de áudio que implementam as interfaces [XAPO](xapo-overview.md) para uso no XAudio2. XAPOFX contém vários efeitos e um mecanismo comum para a criação de instâncias de efeito.

## <a name="included-effects"></a>Efeitos incluídos

A tabela a seguir descreve os efeitos incluídos no XAPOFX. 

| Efeito             | Descrição                                                                                                                                                                                           | Estrutura de parâmetros                                                     | Constantes de parâmetro                                              | Requisitos                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| FXECHO             | Um efeito de eco.                                                                                                                                                                                       | [**parâmetros de FXECHO \_**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                         | [**Constantes FXECHO**](fxecho-constants.md)                     | Dá suporte apenas a formatos de áudio FLOAT32.                                                                                      |
| FXEQ               | Um equalizador de quatro faixas.                                                                                                                                                                                | [**parâmetros de FXEQ \_**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                             | [**Constantes FXEQ**](fxeq-constants.md)                         | Dá suporte apenas a formatos de áudio FLOAT32. A taxa de amostra deve estar entre 22.000 Hz e 48.000 Hz.                             |
| FXMasteringLimiter | Um limitador de volume.                                                                                                                                                                                     | [**parâmetros de FXMASTERINGLIMITER \_**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters) | [**Constantes FXMASTERINGLIMIT**](fxmasteringlimit-constants.md) | Dá suporte apenas a formatos de áudio FLOAT32.                                                                                      |
| FXReverb           | Um efeito simples de reverberação.<br/> O XAudio2 também fornece um efeito para implementar o Princeton digital reverbs que pode ser instanciado com [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb).<br/> | [**parâmetros de FXREVERB \_**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                     | [**Constantes FXREVERB**](fxreverb-constants.md)                 | Dá suporte apenas a formatos de áudio FLOAT32. Além disso, ele só dá suporte à entrada mono para saída mono e entrada estéreo para saída estéreo. |



 

## <a name="creating-an-instance-of-an-effect-included-in-xapofx"></a>Criando uma instância de um efeito incluído no XAPOFX

XAPOFX fornece a função [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) como um mecanismo comum para criar instâncias de efeito. **CreateFX** usa o CLSID de um efeito e retorna um ponteiro de interface IUnknown para uma instância do efeito.

## <a name="using-xapofx-in-xaudio2"></a>Usando XAPOFX no XAudio2

Os efeitos instanciados com [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) são usados em XAudio2 anexando-os às vozes. Cada voz do XAudio2 tem uma cadeia de efeitos que contém zero ou mais efeitos de áudio. Os dados de áudio enviados a uma voz são passados por cada efeito na cadeia antes de serem enviados para os destinos de saída da voz. A voz usa a saída de cada efeito e a alimenta para o próximo efeito na cadeia até que não haja nenhum efeito na cadeia. Para anexar um efeito de XAPOFX a uma voz XAudio2, preencha uma estrutura de [**\_ \_ cadeia de efeito de XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) com as informações do efeito e passe-a para [**IXAudio2Voice:: SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain).

Para obter mais informações sobre cadeias de efeito de XAudio2, consulte [efeitos de áudio XAudio2](xaudio2-audio-effects.md).

Para obter um exemplo de como usar XAPOFX em XAudio2, consulte [como: usar xapofx no XAudio2](how-to--use-xapofx-in-xaudio2.md).

## <a name="xaudio2-implicit-effects"></a>XAudio2 efeitos implícitos

Além da biblioteca de XAPOs fornecida pelo XAPOFX, XAudio2 tem efeitos internos de entrada e de medidor de volume de áudio. Você pode criar esses efeitos internos com [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) e [**XAudio2CreateVolumeMeter**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter). Consulte [como: criar uma cadeia de efeito](how-to--create-an-effect-chain.md) para obter um exemplo de como usar um desses efeitos internos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> </dl>

 

 
