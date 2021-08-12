---
description: Você pode usar a ferramenta Logman para coletar informações de rastreamento para aplicativos VSS que usam o ASR (automated Recuperação do Sistema).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Usando ferramentas de rastreamento com aplicativos ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2d22dbb1488b5fd60836926d3c5ef2de5913ff1cc1529fdb278773b2ccd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590865"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Usando ferramentas de rastreamento com aplicativos ASR

Você pode usar a ferramenta Logman para coletar informações de rastreamento para aplicativos VSS que usam o [ASR (Automated Recuperação do Sistema).](using-vss-automated-system-recovery-for-disaster-recovery.md) O Logman (logman.exe) é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho. Ele está incluído no Windows XP e versões posteriores do Windows. Ou, se preferir, você poderá usar a ferramenta Tracelog para coletar as mesmas informações de rastreamento do ASR. O rastreamento está incluído no WDK (Kit Windows Driver).

Para usar ferramentas de rastreamento com VSS, consulte [Usando ferramentas de rastreamento com VSS.](using-tracing-tools-with-vss.md)

## <a name="using-logman"></a>Usando o Logman

O procedimento a seguir descreve como usar o Logman com seu aplicativo ASR.

**Para usar o Logman com seu aplicativo ASR**

1.  Use o seguinte comando para iniciar o rastreamento:

    **logman start asr -o** *x: \\ ***asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff**

    > [!Note]  
    > Substitua "x: " pelo caminho para o diretório em \\ que você gostaria que o arquivo de log de rastreamento fosse armazenado. Para melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.

     

2.  Use o seguinte comando para interromper o rastreamento:

    **logman stop asr -ets**

O arquivo de log de *rastreamento é x: \\* asr.etl.

Para obter mais informações sobre a ferramenta Logman, consulte [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Usando o Tracelog

O procedimento a seguir descreve como usar o Tracelog.

**Para usar o Tracelog**

1.  Crie um arquivo de texto chamado asr.ctl que contenha apenas o seguinte texto:

    **6407345b-94f2-44c8-b3db-4e076be46816 asr**

2.  Use o seguinte comando para iniciar o rastreamento:

    **tracelog -start asr -f** *x: \\ ***asr.etl -guid asr.ctl -flag 0xff -level 0xff**

    > [!Note]  
    > Substitua "x: " pelo caminho para o diretório em \\ que você gostaria que o arquivo de log de rastreamento fosse armazenado. Para melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.

     

3.  Use o seguinte comando para interromper o rastreamento:

    **tracelog -stop asr**

O arquivo de log de *rastreamento é x: \\* asr.etl.

Para obter mais informações sobre a ferramenta Tracelog, consulte [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
