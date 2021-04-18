---
description: Recursos de suporte a DVD no DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Recursos de suporte a DVD no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035af51bbe44ec8dcc95f199c502b71d37d834f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754255"
---
# <a name="dvd-support-features-in-directshow"></a>Recursos de suporte a DVD no DirectShow

A funcionalidade do filtro [navegador de DVD](dvd-navigator-filter.md) é exposta por meio de duas interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), que fornece os métodos "set" para o navegador de DVD e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), que fornece os métodos "Get".

O navegador de DVD dá suporte aos seguintes recursos:

-   Suporte a karaokê: você pode gravar um aplicativo de DVD-karaokê usando o navegador de DVD. (Isso requer um decodificador compatível.)
-   Acesso simplificado a cadeias de caracteres de informações de texto de DVD: o navegador de DVD analisa essas cadeias de caracteres e permite que os aplicativos enumerem, identifiquem e recuperem facilmente.
-   Controle de volume de áudio por meio de [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Suporte para personalizar o comportamento do navegador de DVD quando o comando de parada é emitido: os aplicativos podem instruir o navegador de DVD a retomar a partir do local atual ao reiniciar o grafo de filtro ou iniciar a reprodução a partir do início do disco.
-   Suporte a áudio de Digital Theater Systems (DTS) e Sony Dynamic Digital Sound (SDDS). Os fluxos de áudio DTS e SDDS são reconhecidos pelo navegador de DVD e passados para o decodificador de áudio. (Um decodificador compatível com DTS de terceiros ou compatível com SDDS é necessário para decodificar e reproduzir o áudio.)
-   Suporte aprimorado para alterações de nível pai: o navegador de DVD permite que um aplicativo aceite, rejeite ou ignore comandos de alteração de nível pai do disco.
-   Opções avançadas para gerenciar o estado do navegador de DVD e a sincronização de comandos
-   Suporte para revisão de quadro, busca com precisão de quadro e reprodução reversa. Esses recursos exigem um decodificador de vídeo que ofereça suporte a eles.
-   A capacidade de salvar o local atual em um título e retornar a ele a qualquer momento.
-   Suporte simplificado para eventos de tempo em títulos de PGC não sequenciais: para títulos de PGC não sequenciais, o navegador de DVD retransmite as informações de código de tempo bruto para o aplicativo.
-   Informações de código de tempo. A estrutura do código de códigos de [**DVD \_ HMSF \_**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) pode ser usada no lugar do formato BCD (decimal codificado binário). **DVD \_ HMSF o \_ código** de tempo contém membros acessados facilmente para horas, minutos, segundos e quadros, e pode ser convertido de/para um **ULONG**.
-   A capacidade de controlar se o grafo de filtro é liberado após uma operação de busca: os buffers de grafo podem conter até alguns segundos de vídeo em um determinado momento. Você pode instruir o grafo a concluir a reprodução do vídeo armazenado em buffer após uma busca ou começar a jogar imediatamente no novo local.
-   A capacidade de definir valores em registros de parâmetros gerais: um recurso avançado para aqueles familiarizados com a especificação de DVD que desejam implementar a funcionalidade avançada.
-   A capacidade de gerar identificadores de disco numéricos que são para todas as finalidades práticas exclusivas

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Em qual plano de fundo eu preciso escrever um aplicativo de DVD?

Todos os desenvolvedores de aplicativos devem ter uma familiaridade básica com os recursos fornecidos pela tecnologia de DVD, como os níveis de gerenciamento de pais, vários fluxos de áudio e subimagem e blocos de ângulo. As [noções básicas de DVD](dvd-basics.md) descrevem brevemente cada um desses recursos; descrições mais completas estão disponíveis em publicações de terceiros. Você não precisa se referir à especificação de DVD, a menos que pretenda implementar recursos avançados além do conjunto de comandos do anexo J.

Os desenvolvedores de C/C++ que usam o DirectShow devem estar familiarizados com técnicas de programação de cliente COM, como criar objetos COM e obter e liberar ponteiros de interface COM. Você também pode precisar de um conhecimento geral das operações de gráfico de filtro, pois talvez seja necessário acessar e manipular o grafo diretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



