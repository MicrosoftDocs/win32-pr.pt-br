---
description: DACL para um novo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para um novo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090921"
---
# <a name="dacl-for-a-new-object"></a>DACL para um novo objeto

O sistema usa o seguinte algoritmo para criar uma DACL para a maioria dos tipos de novos objetos protegíveis:

1.  A DACL do objeto é a DACL do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) especificado pelo criador do objeto. O sistema mescla quaisquer ACEs herdáveis na DACL especificada, a menos que o \_ bit de controle de DACL \_ protegido seja definido nos bits de controles do descritor de segurança.
2.  Se o criador não especificar um descritor de segurança, o sistema criará a DACL do objeto de ACEs herdáveis.
3.  Se nenhum descritor de segurança for especificado e não houver ACEs herdáveis, a DACL do objeto será a DACL padrão do token [*primário*](/windows/desktop/SecGloss/p-gly) ou de [*representação*](/windows/desktop/SecGloss/i-gly) do criador.
4.  Se não houver nenhuma DACL especificada, herdada ou padrão, o sistema criará o objeto sem nenhuma DACL, o que permitirá que todos tenham acesso completo ao objeto.

O sistema usa um algoritmo diferente para criar uma DACL para um novo objeto Active Directory. Para obter mais informações, consulte [como descritores de segurança são definidos em novos objetos de diretório](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
