---
description: O provedor WMIPerfClass e o provedor WMIPerfInst fornecem dinamicamente dados do contador de desempenho para as classes do contador de desempenho do WMI.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Bibliotecas de desempenho e WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765637"
---
# <a name="performance-libraries-and-wmi"></a>Bibliotecas de desempenho e WMI

O [provedor WMIPerfClass](wmiperfclass-provider.md) e o [provedor WMIPerfInst](wmiperfinst-provider.md) fornecem dinamicamente dados do contador de desempenho para as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI.

## <a name="wmiperfclass-and-wmiperfinst-providers"></a>Provedores de WMIPerfClass e WMIPerfInst

O [provedor WMIPerfClass](wmiperfclass-provider.md) cria [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI na inicialização do sistema. O [provedor WMIPerfInst](wmiperfinst-provider.md) fornece dinamicamente dados do contador de desempenho para essas classes. O provedor do provedor WMIPerfClass fornece classes para os [contadores de desempenho](/windows/desktop/PerfCtrs/performance-counters-portal)da versão 1 e da versão 2.

Os contadores da versão 1 são encontrados no registro em **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**. Os serviços que fornecem dados de desempenho têm uma subchave de **desempenho** . As classes de desempenho WMI criadas a partir dos contadores da versão 1 não têm "contadores" como parte do nome.

Os **GUIDs** que identificam um provedor de contador de desempenho versão 2 são encontrados no registro em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.

WMIPerfClass é registrado como um provedor de classe WMI normal. WMIPerfInst é um provedor de instância do WMI que fornece dados do PDH (auxiliar de dados de desempenho) para os contadores da versão 1 e da versão 2. Para obter mais informações, consulte [usando as funções de PDH para consumir dados de contador](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
