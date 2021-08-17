---
title: Estendendo o esquema
description: O esquema do serviço de diretório Active Directory define os atributos e as classes usados no Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, esquema, estendendo o esquema
- esquema de AD, estendendo o esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189554"
---
# <a name="extending-the-schema"></a>Estendendo o esquema

O esquema do serviço de diretório Active Directory define os atributos e as classes usados no Active Directory Domain Services. O esquema base incluído no sistema contém um conjunto avançado de definições de classe, como **User**, **Computer** e **OrganizationalUnit**, e definições de atributo, como **userPrincipalName**, **telephoneNumber** e **objectSid**. O conjunto existente de classes e atributos será suficiente para a maioria dos aplicativos. No entanto, o esquema é extensível, o que significa que você pode definir novas classes e atributos. Esta seção discute como estender o esquema de Active Directory.

## <a name="when-to-extend-the-schema"></a>Quando estender o esquema

Se as classes e os atributos existentes não couberem com o tipo de dados que você deseja armazenar, você deverá estender o esquema. É importante observar que as adições de esquema são permanentes; Você pode desabilitar classes e atributos, mas nunca pode removê-los do esquema. Tenha isso em mente ao testar o código.

Considere também o tamanho dos dados que você deseja armazenar. A Microsoft recomenda que nenhum valor de atributo exceda 500 quilobytes, incluindo a soma de atributos com valores de multivalor. Além disso, os objetos não devem exceder 1 megabyte de tamanho. Considere também o número de instâncias dos dados; Se você adicionar um novo atributo à classe de [**usuário**](/windows/desktop/ADSchema/c-user) em um sistema que tenha 100.000 usuários, isso poderá usar um espaço considerável.

Os tópicos desta seção incluem:

-   Como associar ao contêiner de esquema e ler as propriedades de classes e atributos existentes.
-   Como e quando estender o esquema definindo novos atributos e classes.
-   Como instalar extensões de esquema usando LDIFDE, CSVDE ou programaticamente com ADSI.

Para obter mais informações e uma visão geral do esquema de Active Directory, incluindo informações sobre a implementação do esquema, definições de classe e definições de atributo, consulte [Active Directory esquema](active-directory-schema.md).

Para obter mais informações, incluindo páginas de referência para as classes de esquema predefinidas, atributos e sintaxes de atributo, consulte a referência de esquema de Active Directory na [referência de Active Directory Domain Services](active-directory-domain-services-reference.md).

 

 