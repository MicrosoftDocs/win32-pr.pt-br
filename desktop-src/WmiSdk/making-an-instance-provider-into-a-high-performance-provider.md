---
description: Não é recomendável escrever um provedor WMI de alto desempenho para criar contadores de desempenho.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Criando um provedor de instância em um provedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789221"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a>Criando um provedor de instância em um provedor de High-Performance

Não é recomendável escrever um provedor WMI de alto desempenho para criar contadores de desempenho. A partir do Windows Vista, as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI não são mais migradas para as bibliotecas de desempenho do Windows pelo adaptador reverso de autodescoberta/autolimpeza (ADAP). Para criar um provedor de contador de desempenho, use [contadores de desempenho versão 2,0](/windows/desktop/PerfCtrs/performance-counters-portal). Depois que os objetos de biblioteca de desempenho são criados, o [provedor WMIPerfClass](wmiperfclass-provider.md) analisa os objetos e cria ou atualiza uma classe WMI derivada [**do \_ desempenho do Win32**](/windows/desktop/CIMWin32Prov/win32-perf) para cada objeto de desempenho. O [provedor WMIPerfInst](wmiperfinst-provider.md) , em seguida, fornece dinamicamente dados de contador de desempenho brutos e formatados para as classes de desempenho WMI.

O procedimento de alto nível a seguir fornece as etapas necessárias para criar um provedor de alto desempenho.

**Para criar um provedor de alto desempenho**

1.  Registre seu provedor com o WMI. Para obter mais informações, consulte [registrando um provedor de High-Performance](registering-a-high-performance-provider.md).
2.  Implemente seu provedor. Para obter mais informações, consulte [escrevendo um provedor de instância](writing-an-instance-provider.md).
3.  Implemente a interface de alto desempenho. Para obter mais informações, consulte [implementando a Interface High-Performance](implementing-the-high-performance-interface.md).
4.  Derive e escreva seu esquema de formato MOF (MOF) para obter dados brutos de desempenho. Para obter mais informações, consulte [dando suporte à \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).
5.  Derive e grave seu esquema MOF para obter dados pré-calculados. Ao dar suporte a essa classe, o provedor não precisa executar os cálculos. Esses dados serão os mesmos que aparecem no monitor do sistema no perfmon. Para obter mais informações, consulte [dando suporte à \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
