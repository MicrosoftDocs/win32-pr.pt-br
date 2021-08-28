---
description: O provedor WMIPerfClass e o provedor WMIPerfInst fornecem dinamicamente dados do contador de desempenho para as Classes do Contador de Desempenho do WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de desempenho e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877623bcf27dffe71146df4f9c117da83941bd1d8e2ed46436a04c1d7ace95df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996406"
---
# <a name="performance-libraries-and-wmi"></a>Bibliotecas de desempenho e WMI

O [provedor WMIPerfClass](wmiperfclass-provider.md) e o provedor [WMIPerfInst fornecem dinamicamente](wmiperfinst-provider.md) dados do contador de desempenho para as Classes de Contador de Desempenho [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes).

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Provedores WMIPerfClass e WMIPerfInst

[O provedor WMIPerfClass](wmiperfclass-provider.md) cria classes de contador [de](/windows/desktop/CIMWin32Prov/performance-counter-classes) desempenho WMI na inicialização do sistema. O [provedor WMIPerfInst fornece](wmiperfinst-provider.md) dinamicamente dados do contador de desempenho para essas classes. O provedor provedor WMIPerfClass fornece classes para contadores de desempenho das versões 1 e [2.](/windows/desktop/PerfCtrs/performance-counters-portal)

Os contadores da versão 1 são encontrados no Registro em **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services**. Os serviços que fornecem dados de desempenho têm uma **sub-chave** Desempenho. As classes de desempenho WMI criadas com base nos contadores da versão 1 não têm "Contadores" como parte de seu nome.

Os **GUID** que identificam um provedor de contador de desempenho versão 2 são encontrados no Registro em **HKEY LOCAL MACHINE SOFTWARE \_ Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass é registrado como um provedor de classe WMI normal. WMIPerfInst é um provedor de instância WMI que fornece dados do PDH (Performance Data Helper) para contadores da versão 1 e da versão 2. Para obter mais informações, [consulte Usando as funções PDH para consumir dados do contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
