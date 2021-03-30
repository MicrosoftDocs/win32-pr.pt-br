---
title: Componentes do descritor de segurança
description: Depois de usar o método IADs. Get para recuperar um ponteiro de interface IADsSecurityDescriptor, você pode usar as propriedades IADsSecurityDescriptor para ler ou gravar os componentes do descritor de segurança de um objeto de diretório.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- AD de componentes do descritor de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640380"
---
# <a name="security-descriptor-components"></a>Componentes do descritor de segurança

Depois de usar o método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar um ponteiro de interface [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) , você pode usar as propriedades **IADsSecurityDescriptor** para ler ou gravar os componentes do descritor de segurança de um objeto de diretório. Por exemplo, para obter ou definir a DACL do objeto, use a propriedade [**DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) .

Um descritor de segurança pode armazenar os seguintes dados:

-   Um SID (identificador de segurança) que identifica o proprietário do objeto: o proprietário de um objeto tem o direito implícito de modificar a DACL e os dados do proprietário no descritor de segurança do objeto.
-   Uma DACL (lista de controle de acesso discricionário) que identifica os usuários e grupos que podem executar várias operações no objeto: uma DACL contém uma lista de ACEs (entradas de controle de acesso). Cada ACE permite ou nega um conjunto especificado de direitos de acesso a uma conta de usuário, conta de grupo ou outro confiável especificado. Para obter mais informações, consulte [recuperando a DACL de um objeto](retrieving-an-objectampaposs-dacl.md).
-   Uma SACL (lista de controle de acesso) do sistema que controla como o sistema audita tentativas de acessar o objeto: cada ACE em uma SACL especifica os tipos de tentativas de acesso que geram uma entrada de log de auditoria para uma conta de usuário especificada, conta de grupo ou outro objeto de confiança. Para obter mais informações, consulte [recuperando a SACL de um objeto](retrieving-an-objectampaposs-sacl.md).
-   Um conjunto de sinalizadores de controle do **descritor de segurança que qualifica o significado \_ \_** de um descritor de segurança ou seus componentes: por exemplo, o sinalizador **\_ \_ protegido de DACL do se** protege a DACL do descritor de segurança de herdar ACEs de seu objeto pai.
-   Um SID (identificador de segurança) que identifica o grupo primário do objeto: Active Directory Domain Services não use esse componente.

Para obter mais informações e um exemplo de código que pode ser usado para ler e exibir os dados em um descritor de segurança de objeto e DACL, consulte [lendo o descritor de segurança de um objeto](reading-an-objectampaposs-security-descriptor.md).

 

 