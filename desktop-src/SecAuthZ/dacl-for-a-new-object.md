---
description: DACL para um novo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd5b8f8c16919260c4dace5394f864fe987885a7f2203b2b41162b7c41e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782135"
---
# <a name="dacl-for-a-new-object"></a>DACL para um novo objeto

O sistema usa o seguinte algoritmo para criar uma DACL para a maioria dos tipos de novos objetos de segurança:

1.  A DACL do objeto é a DACL do [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança especificado pelo criador do objeto. O sistema mescla todas as ACEs herdáveis na DACL especificada, a menos que o bit ES DACL PROTECTED esteja definido nos bits de controle do descritor \_ \_ de segurança.
2.  Se o criador não especificar um descritor de segurança, o sistema criará a DACL do objeto de ACEs herdáveis.
3.  Se nenhum descritor de segurança for especificado e não houver ACEs herdáveis, a DACL do objeto será a DACL padrão do [*token*](/windows/desktop/SecGloss/i-gly) primário ou de representação do criador. [](/windows/desktop/SecGloss/p-gly)
4.  Se não houver NENHUM DACL especificado, herdado ou padrão, o sistema criará o objeto sem DACL, o que permitirá a todos o acesso completo ao objeto.

O sistema usa um algoritmo diferente para criar uma DACL para um novo objeto do Active Directory. Para obter mais informações, consulte [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
