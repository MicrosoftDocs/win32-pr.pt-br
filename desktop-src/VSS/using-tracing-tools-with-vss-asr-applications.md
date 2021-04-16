---
description: Você pode usar a ferramenta logman para coletar informações de rastreamento para aplicativos VSS que usam a recuperação automatizada do sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Usando ferramentas de rastreamento com aplicativos ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794551"
---
# <a name="using-tracing-tools-with-asr-applications"></a>Usando ferramentas de rastreamento com aplicativos ASR

Você pode usar a ferramenta logman para coletar informações de rastreamento para aplicativos VSS que usam a [recuperação automatizada do sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md). Logman (logman.exe) é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho. Ele está incluído no Windows XP e em versões posteriores do Windows. Ou, se preferir, você pode usar a ferramenta tracelog para coletar as mesmas informações de rastreamento de ASR. O tracelog está incluído no Windows Driver Kit (WDK).

Para usar as ferramentas de rastreamento com o VSS, consulte [usando ferramentas de rastreamento com o VSS](using-tracing-tools-with-vss.md).

## <a name="using-logman"></a>Usando logman

O procedimento a seguir descreve como usar o logman com seu aplicativo ASR.

**Para usar logman com seu aplicativo ASR**

1.  Use o seguinte comando para iniciar o rastreamento:

    **logman start ASR-o** *x: \\ * * * ASR. etl-ETS-p {6407345b-94F2-44c8-b3db-4e076be46816} 0xFF 0xFF**

    > [!Note]  
    > Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado. Para obter o melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.

     

2.  Use o seguinte comando para interromper o rastreamento:

    **logman Stop ASR-ETS**

O arquivo de log de rastreamento é *x: \\* ASR. etl.

Para obter mais informações sobre a ferramenta Logman, consulte [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Usando tracelog

O procedimento a seguir descreve como usar o tracelog.

**Para usar o tracelog**

1.  Crie um arquivo de texto chamado ASR. CTL que contenha apenas o seguinte texto:

    **6407345b-94F2-44c8-b3db-4e076be46816 ASR**

2.  Use o seguinte comando para iniciar o rastreamento:

    **tracelog-iniciar ASR-f** *x: \\ * * * ASR. etl-GUID ASR. CTL-Flag* 0xFF*

    > [!Note]  
    > Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado. Para obter o melhor desempenho, o arquivo de log de rastreamento deve estar localizado em um volume que não faz parte da cópia de sombra.

     

3.  Use o seguinte comando para interromper o rastreamento:

    **tracelog-parar ASR**

O arquivo de log de rastreamento é *x: \\* ASR. etl.

Para obter mais informações sobre a ferramenta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
