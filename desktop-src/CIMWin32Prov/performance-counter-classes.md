---
description: As classes do Contador de Desempenho permitem acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes.
ms.assetid: 71746363-6fec-4344-8c5e-5cc057ebdf76
ms.tgt_platform: multiple
title: Classes de contador de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc66020fc7863153e3e663c7552ee6805b2a676772fdcbf01cd9683a9ec05486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701646"
---
# <a name="performance-counter-classes"></a>Classes de contador de desempenho

As classes do Contador de Desempenho permitem acesso de script e programa aos dados de desempenho do sistema calculados por provedores de alto desempenho existentes. Essas classes consistem em classes brutas de contador de desempenho e classes de contador de desempenho formatadas.

Provedores diferentes fornecem dados de biblioteca de desempenho por meio do WMI. Os [provedores WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider) e [WMIPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider) fornecem classes para contadores de desempenho das versões 1 e [2.](/windows/desktop/PerfCtrs/performance-counters-portal) Esses provedores mantêm a compatibilidade com as classes disponíveis em sistemas operacionais anteriores.

As classes nesta seção são as classes base abstratas usadas para criar classes de contador de desempenho. Essa não é uma lista completa de classes que você pode encontrar em seu sistema operacional. Para obter mais informações, consulte [Bibliotecas de desempenho e WMI](/windows/desktop/WmiSdk/performance-libraries-and-wmi).

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Win32 \_ Perf**](win32-perf.md)
</dt> <dd>

A classe base para as classes de contador de desempenho [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).

</dd> <dt>

[**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md)
</dt> <dd>

uma classe base abstrata para as classes de dados pré-instaladas e calculadas.

</dd> <dt>

[**Win32 \_ PerfRawData**](win32-perfrawdata.md)
</dt> <dd>

A classe base abstrata para todas as classes de contador de desempenho bruto concreta.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Win32 Classes](win32-provider.md)
</dt> </dl>

 

 
