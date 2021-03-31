---
description: A partir do Windows Vista, esse provedor cria as classes do contador de desempenho do WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Provedor de WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011122"
---
# <a name="wmiperfclass-provider"></a>Provedor de WmiPerfClass

A partir do Windows Vista, esse provedor cria as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes)do WMI. Os dados são fornecidos dinamicamente para essas classes de desempenho WMI pelo provedor [WMIPerfInst](wmiperfinst-provider.md) . O processo de descoberta automática/autolimpeza (ADAP) não transfere mais objetos de contador de desempenho para classes de desempenho WMI no repositório WMI. Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

Para obter mais informações, consulte [bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md).

Embora não seja recomendável que você desenvolva novos objetos de desempenho criando um provedor de alto desempenho WMI e dependa do processo do [*adaptador reverso do adap*](gloss-r.md) para transferir os dados para as bibliotecas de desempenho, a exceção é o desenvolvimento de um driver Windows Driver Model que fornece dados de desempenho. Embora o processo do adaptador reverso continue a funcionar para compatibilidade com versões anteriores, o método recomendado é usar os [contadores de desempenho versão 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).

O nome da instância [**\_ \_ Win32Provider**](--win32provider.md) desse provedor é "WmiPerfClass".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de WMI](wmi-providers.md)
</dt> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

 
