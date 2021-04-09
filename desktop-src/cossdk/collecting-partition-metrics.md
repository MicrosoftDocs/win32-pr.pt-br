---
description: Coletando métricas de partição
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Coletando métricas de partição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089059"
---
# <a name="collecting-partition-metrics"></a>Coletando métricas de partição

Em alguns casos, uma organização pode querer coletar informações sobre o uso do aplicativo COM+ para fins de monitoramento, planejamento de capacidade e contabilidade de recursos.

Por exemplo, um provedor de serviços de aplicativo (ASP) pode querer cobrar um cliente pelo uso de recursos. Para fazer isso, o COM+ permite coletar informações de eventos e métricas em uma base por partição.

A maneira de coletar essas informações para uma partição específica é especificando, para cada interface de instrumentação COM+, o membro de ID de partição dentro da estrutura de eventos padrão. A estrutura de eventos é o primeiro valor de uma interface de instrumentação COM+. Para obter mais informações, consulte [interfaces de instrumentação com+](com--instrumentation-interfaces.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o cache de partição](configuring-the-partition-cache.md)
</dt> <dt>

[Agrupando aplicativos em partições](grouping-applications-into-partitions.md)
</dt> <dt>

[Gerenciando partições locais](managing-local-partitions.md)
</dt> <dt>

[Gerenciando partições no Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Configurando direitos administrativos para uma partição](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



