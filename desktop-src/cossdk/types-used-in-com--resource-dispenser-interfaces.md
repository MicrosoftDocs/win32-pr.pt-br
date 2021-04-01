---
description: Tipos usados em interfaces de dispensador de recursos COM+
ms.assetid: f4b3a828-3d66-455c-9b0c-30086f3ffe23
title: Tipos usados em interfaces de dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c4d0f62ec7c61a9bc0f189c1ee02d1868a3242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646435"
---
# <a name="types-used-in-com-resource-dispenser-interfaces"></a>Tipos usados em interfaces de dispensador de recursos COM+

Os tipos a seguir são usados nas interfaces do dispensador de recurso.



| Tipo           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESTYPID**   | Um **DWORD** que identifica um tipo de recurso, não um recurso específico. Um **RESTYPID** é geralmente um ponteiro para uma estrutura na memória do dispensador que descreve o tipo de recurso. O Gerenciador do dispensador não entende (e não precisa entender) essa estrutura na memória do dispensador de recursos. O Gerenciador do dispensador usa **RESTYPID** apenas para se referir a um tipo de recurso dentro de um dispensador de recurso.                                                                                                                                   |
| **RESID**      | Um **DWORD** que identifica um recurso específico, em oposição a um tipo de recurso. Um **Resid** é geralmente um (**void \* *_) que aponta para uma estrutura na memória do dispensador de recursos que representa o recurso. O Gerenciador do dispensador não precisa entender essa estrutura dentro da memória do dispensador de recursos. O Gerenciador do dispensador usa _* Resid** para se referir a um recurso específico dentro de um dispensador de recurso.                                                                                                                                 |
| **SRESID**     | Uma versão de cadeia de caracteres Unicode de **Resid**, usada nos métodos [**IHolder:: TrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-trackresources) e [**IHolder:: UntrackResourceS**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-untrackresources) . Às vezes, as cadeias de caracteres são úteis quando apenas uma pequena quantidade de informações precisam ser registradas sobre um recurso e toda a descrição do recurso pode estar contida no **SRESID**. Em particular, o uso do **SRESID** pode, às vezes, eliminar a necessidade de um mapa no dispensador de recursos quando o recurso representa uma relação entre duas (ou mais) coisas. |
| **TRANSid**    | Identifica uma transação. Esse tipo pode ser convertido para a interface **ITransaction** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **TIMEINSECS** | Indica por quanto tempo um recurso pode ficar inativo antes de ser destruído.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces do dispensador de recursos COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 



