---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 50397050-3b5c-4683-972c-95d9f661b365
ms.tgt_platform: multiple
title: D (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2310ce8b14baf2b57634cfa36ef83c3dab239503632972b67bdc4cc6a9b1f602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924152"
---
# <a name="d-wmi"></a>D (WMI)

[A](gloss-a.md) B [C](gloss-c.md) D [E](gloss-e.md) [F G](gloss-f.md) [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_datetime"></span><span id="WMI.GLOSS_DATETIME"></span>**Datetime**
</dt> <dd>

Consulte [*Datetime cim*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_decoupled_provider"></span><span id="WMI.GLOSS_DECOUPLED_PROVIDER"></span>**provedor desacoplado**
</dt> <dd>

Um provedor hospedado em um processo separado do WMI. Provedores desaplados são a maneira recomendada de instrumentar um aplicativo, pois o provedor pode controlar seu próprio tempo de vida em vez de ser iniciado sempre que um usuário acessa o provedor por meio do WMI.

</dd> <dt>

<span id="wmi.gloss_direct_access"></span><span id="WMI.GLOSS_DIRECT_ACCESS"></span>**acesso direto**
</dt> <dd>

Uma maneira de acessar propriedades e métodos fornecidos pelo WMI em um script como se fossem propriedades de automação e métodos [**de SWbemObject**](swbemobject.md).

Acesso não direto: `VolumeName = MyDisk.Properties_("VolumeName")`

Acesso direto: `VolumeName = MyDisk.VolumeName`

</dd> <dt>

<span id="wmi.gloss_distributed_management_task_force"></span><span id="WMI.GLOSS_DISTRIBUTED_MANAGEMENT_TASK_FORCE"></span>**DMTF (Distributed Management Task Force)**
</dt> <dd>

Uma organização de padrões internacionais que trabalha com os principais fornecedores de tecnologia, incluindo a Microsoft, para conduzir o desenvolvimento, a adoção e a unificação de padrões de gerenciamento e iniciativas para ambientes de Área de Trabalho, Empresa e Internet.

</dd> <dt>

<span id="wmi.gloss_dmtf"></span><span id="WMI.GLOSS_DMTF"></span>**Dmtf**
</dt> <dd>

Consulte *DMTF (Distributed Management Task Force).*

</dd> <dt>

<span id="wmi.gloss_dynamic_class"></span><span id="WMI.GLOSS_DYNAMIC_CLASS"></span>**classe dinâmica**
</dt> <dd>

Uma classe CIM cuja definição é fornecida por um [*provedor*](gloss-p.md) em tempo de executar, conforme necessário. As classes dinâmicas representam objetos [*gerenciados específicos do provedor*](gloss-m.md) e não são armazenadas no [*repositório CIM.*](gloss-c.md) As classes dinâmicas só são *suportadas por instâncias dinâmicas.*

</dd> <dt>

<span id="wmi.gloss_dynamic_instance"></span><span id="WMI.GLOSS_DYNAMIC_INSTANCE"></span>**instância dinâmica**
</dt> <dd>

Uma instância de uma classe CIM fornecida por um [*provedor*](gloss-p.md) quando necessário. Ele não é armazenado no [*repositório CIM.*](gloss-c.md) Instâncias dinâmicas podem ser fornecidas para classes estáticas ou dinâmicas. O suporte dinâmico a instâncias de uma classe permite que um provedor fornece valores de propriedade de [*até minuto.*](gloss-p.md)

</dd> </dl>

 

 



