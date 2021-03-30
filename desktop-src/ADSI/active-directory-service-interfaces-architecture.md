---
title: Arquitetura de interfaces de serviço Active Directory
description: Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico. Esta seção usa representações de objeto COM para ilustrar vários recursos ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- ADSI da arquitetura de interfaces do serviço Active Directory
- ADSI ADSI, sobre, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634900"
---
# <a name="active-directory-service-interfaces-architecture"></a>Arquitetura de interfaces de serviço Active Directory

Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico. Esta seção usa representações de objeto COM para ilustrar vários recursos ADSI.

Na figura de modelo de objeto a seguir, um objeto de sistema de nível superior contém um objeto de namespace para cada provedor ADSI instalado.

![objeto contêiner de namespaces](images/ds2top.png)

Cada um dos objetos de namespace é, em si, um contêiner que contém os nós raiz de nível superior de cada servidor, domínio ou quaisquer outros tipos de objetos do sistema de diretório definidos como raízes em cada serviço de diretório.

A ADSI fornece um conjunto de interfaces e objetos predefinidos para que os aplicativos cliente possam interagir com os serviços de diretório usando um conjunto uniforme de métodos. No entanto, a ADSI pode não fornecer acesso a todos os recursos de um serviço de diretório. Para usar melhor o conjunto de recursos completo de cada serviço de diretório, a ADSI fornece um modelo de esquema que os provedores de serviço de diretório e fornecedores de software de terceiros podem usar para estender recursos além das interfaces fornecidas na ADSI.

Os objetos de contêiner de nó raiz, encontrados dentro de cada objeto de namespace de provedor, incluem um objeto de contêiner de esquema ADSI. Este objeto contém a definição de todos os recursos para esse provedor. Para obter mais informações, consulte [modelo de esquema ADSI](adsi-schema-model.md).

Esta seção inclui os tópicos a seguir:

-   [Active Directory objetos de interfaces de serviço](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md)
-   [Provedor de interfaces de serviço Active Directory](active-directory-service-interfaces-provider.md)
-   [Modelo de esquema ADSI](adsi-schema-model.md)

 

 




