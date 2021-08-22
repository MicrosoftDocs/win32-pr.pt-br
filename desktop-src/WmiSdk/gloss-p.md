---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d426673b-dea2-4f8b-9259-6a17543f70c0
ms.tgt_platform: multiple
title: P (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230d3dba8be620b0d2d473dbf23960fff79cb7c76abc8a686c47a630605318d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050784"
---
# <a name="p-wmi"></a>P (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F G](gloss-f.md) [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L M](gloss-l.md) [](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) P [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_performance_counter"></span><span id="WMI.GLOSS_PERFORMANCE_COUNTER"></span>**contador de desempenho**
</dt> <dd>

Uma propriedade em uma classe de desempenho derivada de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) que armazena dados de desempenho.

</dd> <dt>

<span id="wmi.gloss_performance_object"></span><span id="WMI.GLOSS_PERFORMANCE_OBJECT"></span>**objeto de desempenho**
</dt> <dd>

Um objeto em uma biblioteca de desempenho que armazena dados em contadores. Esses objetos são visíveis no utilitário [*Monitor do*](gloss-s.md) Sistema. Exemplos são objetos Cache e Disco Lógico. Quando transferido para o WMI pelo [*processo do ADAP,*](gloss-a.md) cada objeto se torna duas classes de desempenho WMI. Uma classe, que contém dados brutos, deriva de [**Win32 \_ PerfRawData.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) A outra classe deriva de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) e contém os mesmos dados visíveis no Monitor do Sistema, conforme calculado pelo provedor De contadores preparados.

</dd> <dt>

<span id="wmi.gloss_permanent_consumer"></span><span id="WMI.GLOSS_PERMANENT_CONSUMER"></span>**consumidor permanente**
</dt> <dd>

Um [*consumidor de*](gloss-e.md) eventos cujo registro dura até que seja explicitamente cancelado. Consulte também [*consumidor temporário.*](gloss-t.md)

</dd> <dt>

<span id="wmi.gloss_physical_consumer"></span><span id="WMI.GLOSS_PHYSICAL_CONSUMER"></span>**consumidor físico**
</dt> <dd>

Um objeto COM implementado por um provedor de [*consumidor de eventos*](gloss-e.md) que inclui um sink [*para*](gloss-s.md) receber notificações de eventos.

</dd> <dt>

<span id="wmi.gloss_property"></span><span id="WMI.GLOSS_PROPERTY"></span>**Propriedade**
</dt> <dd>

Um par nome/valor que descreve uma unidade de dados para uma classe. Os valores de propriedade devem ter um [*tipo de Managed Object Format (MOF)*](gloss-m.md) válido. Consulte também [*a propriedade de referência*](gloss-r.md).

</dd> <dt>

<span id="wmi.gloss_property_provider"></span><span id="WMI.GLOSS_PROPERTY_PROVIDER"></span>**provedor de propriedades**
</dt> <dd>

Um servidor COM que dá suporte à recuperação e modificação de propriedades WMI. Os provedores de propriedades implementam as interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemPropertyProvider.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)

</dd> <dt>

<span id="wmi.gloss_provider"></span><span id="WMI.GLOSS_PROVIDER"></span>**Provedor**
</dt> <dd>

Um servidor COM que se comunica com objetos gerenciados para acessar dados e notificações de eventos, como o registro ou um dispositivo SNMP. Os provedores encaminham esses dados para o [*Gerenciador de Objetos CIM*](gloss-c.md) para integração e interpretação.

</dd> <dt>

<span id="wmi.gloss_provider_method"></span><span id="WMI.GLOSS_PROVIDER_METHOD"></span>**método provider**
</dt> <dd>

Um método que um provedor *WMI* implementa.

</dd> </dl>

 

 
