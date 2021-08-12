---
description: Tipos usados em interfaces do distribuidor de recursos COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipos usados em interfaces do distribuidor de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e98473ce108ea280532c2188e911b488e42669b98273b14fc229d003905b581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305226"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipos usados em interfaces do distribuidor de recursos COM+

Os tipos a seguir são usados nas interfaces do distribuidor de recursos.



| Type           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | Um **DWORD** que identifica um tipo de recurso, não um recurso específico. Um **RESTYPID** geralmente é um ponteiro para uma estrutura na memória do distribuidor que descreve o tipo de recurso. O gerenciador do distribuidor não entende (e não precisa entender) essa estrutura na memória do distribuidor de recursos. O gerenciador do distribuidor usa **RESTYPID** apenas para se referir a um tipo de recurso dentro de um distribuidor de recursos.                                                                                                                                   |
| **Resid**      | Um **DWORD** que identifica um recurso específico, em vez de um tipo de recurso. Um **RESID** geralmente é um ( void _) que aponta para uma estrutura na memória do distribuidor de recursos **que representa o \* *recurso. O gerenciador do distribuidor não precisa entender essa estrutura na memória do distribuidor de recursos. O gerenciador do distribuidor usa _* RESID** para se referir a um recurso específico dentro de um distribuidor de recursos.                                                                                                                                 |
| **SRESID**     | Uma versão de cadeia de caracteres Unicode de **RESID**, usada nos métodos [**IHolder::TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) e [**IHolder::UntrackResourceS.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) Às vezes, as cadeias de caracteres são úteis quando apenas uma pequena quantidade de informações precisa ser registrada sobre um recurso e toda a descrição do recurso pode estar contida no **SRESID.** Em particular, usar **o SRESID** às vezes pode eliminar a necessidade de um mapa no distribuidor de recursos quando o recurso representa uma relação entre duas (ou mais) coisas. |
| **TRANSID**    | Identifica uma transação. Esse tipo pode ser transferido para a interface **ITransaction.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica por quanto tempo um recurso pode ficar inativo antes de ser destruído.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Com+ Resource Dispenser](com--resource-dispenser-concepts.md)
</dt> <dt>

[COM+ Resource Dispenser Interfaces](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



