---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d469b94ec6649c64722fb414880d2e79fc3c88b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011126"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**horário**
</dt> <dd>

Consulte [*data e hora do CIM*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**provedor dissociado**
</dt> <dd>

Um provedor hospedado em um processo separado do WMI. Os provedores dissociados são a maneira recomendada para instrumentar um aplicativo, pois o provedor pode controlar seu próprio tempo de vida em vez de ser iniciado sempre que um usuário acessa o provedor por meio do WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**acesso direto**
</dt> <dd>

Uma maneira de acessar propriedades e métodos fornecidos pelo WMI em um script como se fossem Propriedades de automação e métodos de [**SWbemObject**](swbemobject.md).

Acesso não direto: `VolumeName = MyDisk.Properties_("VolumeName")`

Acesso direto: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**DMTF (Distributed Management Task Force)**
</dt> <dd>

Uma organização de padrões internacionais que funciona com os principais fornecedores de tecnologia, incluindo a Microsoft, para liderar o desenvolvimento, a adoção e a Unificação de padrões de gerenciamento e iniciativas para ambientes de área de trabalho, empresariais e Internet.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**DMTF**
</dt> <dd>

Consulte *DMTF (Distributed Management Task Force)*.

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dinâmica**
</dt> <dd>

Uma classe CIM cuja definição é fornecida por um [*provedor*](gloss-p.md) em tempo de execução, conforme necessário. Classes dinâmicas representam [*objetos gerenciados*](gloss-m.md) específicos do provedor e não são armazenadas no [*repositório CIM*](gloss-c.md). Classes dinâmicas dão suporte apenas a *instâncias dinâmicas*.

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**instância dinâmica**
</dt> <dd>

Uma instância de uma classe CIM fornecida por um [*provedor*](gloss-p.md) quando necessário. Ele não é armazenado no [*repositório CIM*](gloss-c.md). Instâncias dinâmicas podem ser fornecidas para classes estáticas ou dinâmicas. O suporte dinâmico a instâncias de uma classe permite que um provedor forneça valores de [*Propriedade*](gloss-p.md) de até o minuto.

</dd> </dl>

 

 



