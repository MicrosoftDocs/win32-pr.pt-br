---
title: Mapeando Waveform-Audio dispositivos
description: Mapeando Waveform-Audio dispositivos
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- áudio multimídia, mapeando dispositivos waveform-audio
- áudio, mapeando dispositivos waveform-audio
- gerenciador de compactação de áudio (ACM), mapeando dispositivos waveform-audio
- ACM (gerenciador de compactação de áudio), mapeando dispositivos waveform-audio
- mapeando dispositivos waveform-audio
- áudio multimídia, mapeado
- audio,mapper
- gerenciador de compactação de áudio (ACM), mapeado
- ACM (gerenciador de compactação de áudio), mapeado
- mapper
- áudio waveform, mapeando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4204a79eebd5fed3c8f96712aa3cd83c50056b1c194bafe2ce485a5b4b68f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138767"
---
# <a name="mapping-waveform-audio-devices"></a>Mapeando Waveform-Audio dispositivos

Windows fornece um conjunto de funções padrão para dispositivos de áudio. Essas funções em emitir chamadas para drivers de dispositivo que gerenciam dispositivos de hardware. O sistema usa um módulo chamado "mapeado" para gerenciar dispositivos instalados. O mapeado usa ganchos especiais na interface do driver para interceptar chamadas e atuar como um intermediário entre o sistema e os drivers instalados no sistema. O mapeado é responsável por corresponder as solicitações de acesso de um aplicativo a um dispositivo com os dispositivos disponíveis e encontrar um dispositivo que atenda aos requisitos de áudio do aplicativo atual. O sistema fornece mapeados para tipos de driver padrão: waveform-audio, MIDI (Instrument Digital Interface Digital) e dispositivos auxiliares.

O ACM é uma extensão do sistema multimídia básico e é instalado como um mapeado. Isso significa que o ACM usa os ganchos mapeados da interface do driver para dispositivos waveform-audio. O uso desses ganchos permite que o ACM decodificar ou codificar dados waveform-audio antes de passá-los para ou de um driver de dispositivo waveform-audio. A diferença entre o ACM e o mapeador de sistema padrão é que o ACM pode pesquisar um dispositivo waveform-audio que dá suporte a um formato especificado ou encontrar uma combinação de um dispositivo waveform-audio e um descompactador ou um ACM que dá suporte a um formato especificado.

Quando um aplicativo solicita que o sistema abra um dispositivo waveform-audio para entrada ou saída, a solicitação especifica o formato e o dispositivo. Quando o dispositivo especificado é o mapeado, o mapeado deve encontrar um dispositivo que dá suporte ao formato especificado. O mapeado implementado no ACM pesquisa um dispositivo waveform-audio instalado que dá suporte ao formato especificado. Se o ACM não conseguir encontrar esse dispositivo, ele procurará um dispositivo waveform-audio e um descompactador ou um descompactador que, juntos, suportam o formato. Especificamente, o ACM pesquisa um descompactador ou um descompactador que converte o formato especificado em um formato com suporte de um dispositivo waveform-audio instalado. Depois que o ACM encontrar um dispositivo que dá suporte ao formato convertido, ele poderá manter as solicitações para reproduzir ou registrar o formato originalmente solicitado, mesmo que nenhum dispositivo waveform-audio instalado seja compatível diretamente com esse formato.

Além da conversão de formato, o ACM também oferece serviços para dar suporte à compactação, descompactação, filtragem, seleção de formato e seleção de filtro. Ele fornece uma API padrão que dá suporte chamando seus próprios drivers.

 

 




