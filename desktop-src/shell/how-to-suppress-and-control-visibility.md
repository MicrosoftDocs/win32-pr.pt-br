---
description: Este tópico mostra como controlar a visibilidade de verbo.
title: Como suprimir e controlar a visibilidade de verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169426"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a>Como suprimir e controlar a visibilidade de verbo

Este tópico mostra como controlar a visibilidade de verbo.

## <a name="instructions"></a>Instruções


Você pode usar as configurações da política do Windows para controlar a visibilidade do verbo. Os verbos podem ser suprimidos por meio de configurações de política adicionando uma subchave **SuppressionPolicy** ou um valor de GUID **SuppressionPolicyEx** à subchave do registro do verbo. Defina o valor da subchave **SuppressionPolicy** para a ID da política. Se a política for ativada, o verbo e sua entrada de menu de atalho associada serão suprimidos. Para obter possíveis valores de ID de política, consulte a enumeração de [**restrições**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

 

 



