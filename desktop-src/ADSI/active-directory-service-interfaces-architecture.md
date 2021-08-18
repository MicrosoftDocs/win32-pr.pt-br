---
title: Arquitetura de interfaces de serviço do Active Directory
description: Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico. Esta seção usa representações de objeto COM para ilustrar vários recursos adsi.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Arquitetura adsi de interfaces de serviço do Active Directory
- ADSI ADSI, sobre, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afbc212edbea6491de4cae89f2c8b7c873019b6d5678c5bf1d5b531f519260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024075"
---
# <a name="active-directory-service-interfaces-architecture"></a>Arquitetura de interfaces de serviço do Active Directory

Muitos serviços de diretório são hierárquicos e, portanto, prestam-se a um modelo de objeto hierárquico. Esta seção usa representações de objeto COM para ilustrar vários recursos adsi.

Na figura do modelo de objeto a seguir, um objeto de sistema de nível superior contém um objeto namespace para cada provedor ADSI instalado.

![objeto de contêiner namespaces](images/ds2top.png)

Cada um dos objetos namespace é um contêiner que contém os nós raiz de nível superior de cada servidor, domínio ou quaisquer outros tipos de objetos do sistema de diretório são definidos como raízes em cada serviço de diretório.

A ADSI fornece um conjunto de objetos e interfaces predefinidos para que os aplicativos cliente possam interagir com os serviços de diretório usando um conjunto uniforme de métodos. No entanto, a ADSI pode não fornecer acesso a todos os recursos de um serviço de diretório. Para usar melhor o conjunto de recursos completo de cada serviço de diretório, a ADSI fornece um modelo de esquema que provedores de serviços de diretório e fornecedores de software de terceiros podem usar para estender recursos além das interfaces fornecidas no ADSI.

Os objetos de contêiner de nó raiz, encontrados dentro de cada objeto namespace do provedor, incluem um objeto de contêiner de esquema ADSI. Esse objeto contém a definição de todos os recursos para esse provedor. Para obter mais informações, consulte [Modelo de esquema ADSI](adsi-schema-model.md).

Esta seção inclui os tópicos a seguir:

-   [Objetos de interfaces de serviço do Active Directory](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md)
-   [Provedor de Interfaces de Serviço do Active Directory](active-directory-service-interfaces-provider.md)
-   [Modelo de esquema ADSI](adsi-schema-model.md)

 

 




