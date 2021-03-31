---
title: Mapeando dispositivos Waveform-Audio
description: Mapeando dispositivos Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- áudio de multimídia, mapeamento de formato de onda-dispositivos de áudio
- áudio, mapeamento de formato de onda-dispositivos de áudio
- Gerenciador de compactação de áudio (ACM), mapeamento de formato de onda-dispositivos de áudio
- ACM (Gerenciador de compactação de áudio), mapeamento de formato de onda-dispositivos de áudio
- mapeando a onda-dispositivos de áudio
- áudio de multimídia, mapeador
- áudio, mapeador
- Gerenciador de compactação de áudio (ACM), mapeador
- ACM (Gerenciador de compactação de áudio), mapeador
- mapper
- áudio de onda, dispositivos de mapeamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822491"
---
# <a name="mapping-waveform-audio-devices"></a>Mapeando dispositivos Waveform-Audio

O Windows fornece um conjunto de funções padrão para dispositivos de áudio. Essas funções emitem chamadas para drivers de dispositivo que gerenciam dispositivos de hardware. O sistema usa um módulo chamado "mapeador" para gerenciar os dispositivos instalados. O mapeador usa ganchos especiais na interface do driver para interceptar chamadas e agir como um intermediário entre o sistema e os drivers instalados no sistema. O mapeador é responsável por corresponder as solicitações de um aplicativo para acesso a um dispositivo com os dispositivos disponíveis e para localizar um dispositivo que atenda aos requisitos de áudio do aplicativo atual. O sistema fornece Mapeadores para tipos de driver padrão: wave-áudio, MIDI (interface digital de instrumentos musicais) e dispositivos auxiliares.

O ACM é uma extensão do sistema de multimídia básico e é instalado como um mapeador. Isso significa que o ACM usa os ganchos do mapeador de interface de driver para dispositivos de forma de onda-áudio. O uso desses ganchos permite que o ACM decodifique ou codifique dados de wave-áudio antes de passá-los para ou de um driver de dispositivo de forma de onda-áudio. A diferença entre o ACM e o mapeador de sistema padrão é que o ACM pode pesquisar um dispositivo de wave-áudio que dá suporte a um formato especificado ou encontrar uma combinação de um dispositivo de wave-áudio e um compressor ou descompactador ACM que dá suporte a um formato especificado.

Quando um aplicativo solicita que o sistema abra um dispositivo de forma de onda-áudio para entrada ou saída, a solicitação especifica o formato e o dispositivo. Quando o dispositivo especificado é o mapeador, o mapeador deve localizar um dispositivo que ofereça suporte ao formato especificado. O mapeador implementado no ACM pesquisa um dispositivo de wave-áudio instalado que dá suporte ao formato especificado. Se o ACM não puder encontrar esse dispositivo, ele pesquisará um dispositivo de wave-áudio e um compressor ou descompactador que juntos dão suporte ao formato. Especificamente, o ACM procura um compressor ou descompactador que converte o formato especificado em um formato com suporte de um dispositivo de wave-áudio instalado. Depois que o ACM encontra um dispositivo que dá suporte ao formato convertido, ele pode honrar solicitações para reproduzir ou registrar o formato solicitado originalmente, mesmo que nenhum dispositivo de Wave de som instalado ofereça suporte diretamente a esse formato.

Além da conversão de formato, o ACM também oferece serviços para dar suporte à compactação, descompactação, filtragem, seleção de formato e seleção de filtro. Ele fornece uma API padrão que ele suporta chamando seus próprios drivers.

 

 




