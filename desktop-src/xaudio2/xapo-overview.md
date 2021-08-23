---
description: A API XAPO permite a criação de objetos de processamento de áudio de plataforma cruzada (XAPO) para uso no XAudio2 em Windows e Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Visão geral do XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ee64e865c8e3ef3cdac026274b922db438a54979dcb30d855a92b96e4e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589906"
---
# <a name="xapo-overview"></a>Visão geral do XAPO

A API XAPO permite a criação de objetos de processamento de áudio de plataforma cruzada (XAPO) para uso no XAudio2 em Windows e Xbox 360. Um XAPO é um objeto que recebe dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um XAPO para executar uma variedade de tarefas, incluindo adicionar reverb a um fluxo de áudio e monitorar níveis de volume de pico.

## <a name="creating-new-xapos"></a>Criando novos XAPOs

A API XAPO fornece a interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e a [**classe CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para a criação de novos tipos de XAPO. A interface **IXAPO** contém todos os métodos que precisam ser implementados para criar um novo XAPO. A **classe CXAPOBase** fornece uma implementação básica da interface **IXAPO.** **O CXAPOBase** implementa todos os métodos de interface **IXAPO,** exceto o método [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que é exclusivo para cada XAPO.

Para ver um exemplo de criação de um novo XAPO, [consulte Como criar um XAPO.](how-to--create-an-xapo.md)

Para ver um exemplo de criação de um XAPO que aceita parâmetros de tempo de run-time, consulte Como adicionar suporte a parâmetros em tempo de [run-time a um XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs e COM

Os XAPOs implementam a interface **IUnknown.** As interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluem os três métodos **IUnknown:** **QueryInterface,** **AddRef** e **Release**. [**O CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornece implementações de todos os três métodos IUnknown. Uma nova instância do **CXAPOBase** terá uma contagem de referência de 1. Ele será destruído quando sua contagem de referência se tornar 0. Implementações de **IXAPO** e **IXAPOParameters** devem seguir o mesmo padrão para permitir o gerenciamento adequado quando usados com XAudio2.

As instâncias XAPO são passadas para XAudio2 como interfaces **IUnknown.** O XAudio2 usa **QueryInterface** para adquirir uma interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e detectar se o XAPO implementa a interface [**IXAPOParameters.**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) Implementações de **IXAPO** devem aceitar solicitações para **\_ \_ uuidof(IXAPO).** Se **IXAPOParameters** for implementado, ele também deverá aceitar solicitações para **\_ \_ uuidof(IXAPOParameters).**

## <a name="using-an-xapo-in-xaudio2"></a>Usando um XAPO no XAudio2

Os XAPOs são usados no XAudio2 anexando-os às vozes. Cada voz XAudio2 tem uma cadeia de efeitos que contém zero ou mais efeitos de áudio. Os dados de áudio enviados a uma voz são passados por meio de cada efeito na cadeia antes que eles são enviados para os destinos de saída da voz. Os dados são passados da voz para cada efeito usando o *parâmetro pInputProcessParameters* do método [**IXAPO::P rocess.**](/windows/win32/api/xapo/nf-xapo-ixapo-process) Em seguida, ele é retornado à voz usando o *parâmetro pOutputProcessParameters.* A voz assume a saída de cada efeito e a alimenta para o próximo efeito na cadeia até que nenhum efeito seja deixado na cadeia.

Para obter mais informações sobre cadeias de efeito XAudio2, consulte Efeitos de áudio [XAudio2](xaudio2-audio-effects.md).

Para ver um exemplo de como usar um XAPO no XAudio2, consulte Como usar um [XAPO no XAudio2.](how-to--use-an-xapo-in-xaudio2.md)

## <a name="effect-libraries"></a>Bibliotecas de efeito

A biblioteca de efeitos XAPO contém vários XAPOs e um método comum de instaná-los. Consulte [Visão geral do XAPOFX](xapofx-overview.md) para obter informações sobre XAPOFX. Além disso, o XAudio2 tem efeitos de reverb e medidor de volume integrados. Consulte [Efeitos de áudio XAudio2](xaudio2-audio-effects.md) para obter mais informações sobre os efeitos XAudio2 integrados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Efeitos de áudio XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
