---
description: As classes de contador de desempenho permitem o acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d147e5ebc18dfe532ceec7a2fb55bb21c6fa13f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826703"
---
# <a name="performance-counter-classes"></a>Classes de contador de desempenho

As classes de contador de desempenho permitem o acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes. Essas classes consistem em classes de contador de desempenho brutos e classes de contador de desempenho formatadas.

Provedores diferentes fornecem dados de biblioteca de desempenho por meio do WMI. Os provedores [WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) fornecem classes para os [contadores de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)da versão 1 e da versão 2. Esses provedores mantêm a compatibilidade com as classes disponíveis em sistemas operacionais anteriores.

As classes nesta seção são as classes base abstratas usadas para criar classes de contador de desempenho. Essa não é uma lista completa de classes que você pode encontrar em seu sistema operacional. Para obter mais informações, consulte [bibliotecas de desempenho e WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Desempenho do Win32 \_**](win32-perf.md)
</dt> <dd>

A classe base para as classes de contador de desempenho [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**\_PerfFormattedData Win32**](win32-perfformatteddata.md)
</dt> <dd>

uma classe base abstrata para as classes de dados previamente instaladas, calculadas.

</dd> <dt>

[**\_PerfRawData Win32**](win32-perfrawdata.md)
</dt> <dd>

A classe base abstrata para todas as classes de contador de desempenho brutos concretos.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes Win32](win32-provider.md)
</dt> </dl>

 

 
