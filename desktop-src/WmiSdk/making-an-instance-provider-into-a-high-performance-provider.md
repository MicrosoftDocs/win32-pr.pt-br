---
description: Não é recomendável escrever um provedor de alto desempenho WMI para criar contadores de desempenho.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Transformando um provedor de instância em um provedor High-Performance dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b6326c0af270088c37bb2a1798951ba0a9de7afe65ec593f5f7ab6768b83b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996486"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Transformando um provedor de instância em um provedor High-Performance dados

Não é recomendável escrever um provedor de alto desempenho WMI para criar contadores de desempenho. A partir do Windows Vista, as Classes de Contador de Desempenho [WMI](/windows/desktop/CIMWin32Prov/performance-counter-classes) não são mais migradas para as bibliotecas de desempenho Windows pelo adaptador reverso ADAP (Descoberta Automática/Uso Automático). Para criar um provedor de contador de desempenho, use [Contadores de Desempenho versão 2.0](/windows/desktop/PerfCtrs/performance-counters-portal). Depois que os objetos de biblioteca de desempenho são criados, o Provedor [WMIPerfClass](wmiperfclass-provider.md) analisará os objetos e criará ou atualizará uma classe WMI derivada de [**Win32 \_ Perf**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de desempenho. O [provedor WMIPerfInst](wmiperfinst-provider.md) fornece dinamicamente dados brutos e formatados do contador de desempenho para as classes de desempenho WMI.

O procedimento de alto nível a seguir fornece as etapas necessárias para criar um provedor de alto desempenho.

**Para criar um provedor de alto desempenho**

1.  Registre seu provedor com o WMI. Para obter mais informações, [consulte Registrando um provedor High-Performance .](registering-a-high-performance-provider.md)
2.  Implemente seu provedor. Para obter mais informações, consulte [Escrevendo um provedor de instância](writing-an-instance-provider.md).
3.  Implemente a interface de alto desempenho. Para obter mais informações, [consulte Implementando a interface High-Performance .](implementing-the-high-performance-interface.md)
4.  Derive e escreva seu esquema Managed Object Format (MOF) para obter dados brutos de desempenho. Para obter mais informações, consulte [Dando suporte à classe Win32 \_ PerfRawData](supporting-the-win32-perfrawdata-class.md).
5.  Derive e escreva seu esquema MOF para obter dados pré-calculados. Ao dar suporte a essa classe, o provedor não é necessário para executar os cálculos. Esses dados serão os mesmos que aparecem no Monitor do Sistema no Perfmon. Para obter mais informações, consulte [Dando suporte à classe Win32 \_ PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
