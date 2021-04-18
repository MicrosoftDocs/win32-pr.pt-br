---
description: A API do XAPO permite a criação de XAPO (objetos de processamento de áudio de plataforma cruzada) para uso no XAudio2 no Windows e no Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Visão geral do XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815537"
---
# <a name="xapo-overview"></a>Visão geral do XAPO

A API do XAPO permite a criação de XAPO (objetos de processamento de áudio de plataforma cruzada) para uso no XAudio2 no Windows e no Xbox 360. Um XAPO é um objeto que usa dados de áudio de entrada e executa alguma operação nos dados antes de passá-los. Você pode usar um XAPO para executar uma variedade de tarefas, incluindo adicionar reverberação a um fluxo de áudio e monitorar os níveis de volume de pico.

## <a name="creating-new-xapos"></a>Criando novo XAPOs

A API XAPO fornece a interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e a classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para a criação de novos tipos XAPO. A interface **IXAPO** contém todos os métodos que precisam ser implementados para criar um novo XAPO. A classe **CXAPOBase** fornece uma implementação básica da interface **IXAPO** . **CXAPOBase** implementa todos os métodos de interface **IXAPO** , exceto o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que é exclusivo para cada XAPO.

Para obter um exemplo de como criar um novo XAPO, consulte [como: criar um XAPO](how-to--create-an-xapo.md).

Para obter um exemplo de como criar um XAPO que aceite parâmetros de tempo de execução, consulte [como adicionar suporte a parâmetros de tempo de execução a um XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs e COM

XAPOs implemente a interface **IUnknown** . As interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluem os três métodos **IUnknown** : **QueryInterface**, **AddRef** e **Release**. O [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornece implementações de todos os três métodos IUnknown. Uma nova instância de **CXAPOBase** terá uma contagem de referência de 1. Ele será destruído quando sua contagem de referência se tornar 0. As implementações de **IXAPO** e **IXAPOParameters** devem seguir o mesmo padrão para permitir o gerenciamento adequado quando usadas com XAudio2.

As instâncias XAPO são passadas para XAudio2 como interfaces **IUnknown** . O XAudio2 usa **QueryInterface** para adquirir uma interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e detectar se o XAPO implementa a interface [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . As implementações de **IXAPO** devem aceitar solicitações para **\_ \_ uuidof (IXAPO)**. Se **IXAPOParameters** for implementado, ele também deverá aceitar solicitações para **\_ \_ uuidof (IXAPOParameters)**.

## <a name="using-an-xapo-in-xaudio2"></a>Usando um XAPO no XAudio2

XAPOs são usados em XAudio2 anexando-os às vozes. Cada voz do XAudio2 tem uma cadeia de efeitos que contém zero ou mais efeitos de áudio. Os dados de áudio enviados a uma voz são passados por cada efeito na cadeia antes de serem enviados para os destinos de saída da voz. Os dados são passados da voz para cada efeito usando o parâmetro *pInputProcessParameters* do método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) . Em seguida, ele é retornado para a voz usando o parâmetro *pOutputProcessParameters* . A voz usa a saída de cada efeito e a alimenta para o próximo efeito na cadeia até que não haja nenhum efeito na cadeia.

Para obter mais informações sobre cadeias de efeito de XAudio2, consulte [efeitos de áudio XAudio2](xaudio2-audio-effects.md).

Para obter um exemplo de como usar um XAPO no XAudio2, consulte [como: usar um XAPO no XAudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Bibliotecas de efeito

A biblioteca de efeitos XAPO contém vários XAPOs e um método comum de instanciá-los. Consulte [visão geral do xapofx](xapofx-overview.md) para obter informações sobre o xapofx. Além disso, o XAudio2 tem efeitos internos de reverbo e de medidor de volume. Consulte [efeitos de áudio XAudio2](xaudio2-audio-effects.md) para obter mais informações sobre os efeitos de XAudio2 internos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Efeitos de áudio](audio-effects.md)
</dt> <dt>

[Efeitos de áudio XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
