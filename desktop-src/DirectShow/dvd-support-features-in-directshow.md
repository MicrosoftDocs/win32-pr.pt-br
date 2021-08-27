---
description: Recursos de suporte de DVD DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Recursos de suporte de DVD DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107896"
---
# <a name="dvd-support-features-in-directshow"></a>Recursos de suporte de DVD DirectShow

A funcionalidade do filtro Navegador de DVD é exposta por meio de duas interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), que fornece os métodos "set" para o Navegador de [DVD](dvd-navigator-filter.md) e [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)que fornece os métodos "get".

O Navegador de DVD dá suporte aos seguintes recursos:

-   Suporte a Ela: você pode escrever um aplicativo DVD-dvd-dvd usando o Navegador de DVD. (Isso requer um decodificador compatível.)
-   Acesso simplificado a cadeias de caracteres de informações de texto de DVD: o Navegador de DVD analisará essas cadeias de caracteres e permitirá que os aplicativos as enumerem, identifiquem e recuperem facilmente.
-   Controle de volume de áudio por [ **meio de IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Suporte para personalizar o comportamento do Navegador de DVD quando o comando Parar é emitido: os aplicativos podem instruir o Navegador de DVD a retomar do local atual ao reiniciar o grafo de filtro ou iniciar a reprodução desde o início do disco.
-   Suporte a áudio DTS (Digital Sound Systems) e SDDS (Dynamic Digital Sound). Os fluxos de áudio DTS e SDDS são reconhecidos pelo Navegador de DVD e passados para o decodificador de áudio. (Um decodificador compatível com DTS ou SDDS de terceiros é necessário para decodificar e reproduzir o áudio.)
-   Suporte aprimorado para alterações no nível dos pais: o Navegador de DVD permite que um aplicativo aceite, rejeite ou ignore comandos de alteração no nível dos pais do disco.
-   Opções avançadas para gerenciar o estado do Navegador de DVD e comandos de sincronização
-   Suporte para a revisão de quadro, busca com precisão de quadro e reprodução inversa. Esses recursos exigem um decodificador de vídeo que dá suporte a eles.
-   A capacidade de salvar o local atual em um título e retornar a ele a qualquer momento.
-   Suporte simplificado para eventos de tempo em títulos PGC não sequenciais: para títulos PGC não sequenciais, o Navegador de DVD retransmite as informações de código de tempo bruto para o aplicativo.
-   Informações de código de hora. A [**estrutura \_ \_ TIMECODE de DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) pode ser usada no lugar do formato decimal codificado binário (BCD). **DVD \_ O HMSF \_ TIMECODE** contém membros facilmente acessados por horas, minutos, segundos e quadros e pode ser lançado para/de um **ULONG.**
-   A capacidade de controlar se o grafo de filtro é liberado após uma operação de busca: os buffers de grafo podem conter até alguns segundos de vídeo a qualquer momento. Você pode instruir o grafo a concluir a reprodução do vídeo armazenado em buffer após uma busca ou começar a tocar imediatamente no novo local.
-   A capacidade de definir valores em registros de parâmetro geral: um recurso avançado para aqueles familiarizados com a especificação de DVD que desejam implementar a funcionalidade avançada.
-   A capacidade de gerar identificadores de disco numérico que são exclusivos para todas as finalidades práticas

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>Qual plano de fundo preciso para escrever um aplicativo de DVD?

Todos os desenvolvedores de aplicativos devem ter uma familiaridade básica com os recursos fornecidos pela tecnologia de DVD, como níveis de gerenciamento dos pais, vários fluxos de áudio e subtípicos e blocos angulares. [Noções básicas](dvd-basics.md) de DVD descreve brevemente cada um desses recursos; descrições mais completas estão disponíveis em publicações de terceiros. Você não precisa se referir à especificação de DVD, a menos que pretenda implementar recursos avançados além do conjunto de comandos anexo J.

Os desenvolvedores C/C++ que usam DirectShow devem estar familiarizados com técnicas de programação de cliente COM, como criar objetos COM e obter e liberar ponteiros de interface COM. Talvez você também precise de um conhecimento geral das operações de grafo de filtro, pois talvez seja necessário acessar e manipular o grafo diretamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



