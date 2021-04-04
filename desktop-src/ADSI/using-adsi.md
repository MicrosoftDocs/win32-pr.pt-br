---
title: Usando Active Directory interfaces de serviço
description: As interfaces de serviço do Active Directory (ADSI) fornecem os meios para que os aplicativos cliente dos serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que forneça uma implementação de ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Usando Active Directory ADSI de interfaces de serviço
- ADSI, ADSI, usando
- ADSI de interfaces de serviço Active Directory, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822177"
---
# <a name="using-active-directory-service-interfaces"></a>Usando Active Directory interfaces de serviço

As interfaces de serviço do Active Directory (ADSI) fornecem os meios para que os aplicativos cliente dos serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que forneça uma implementação de ADSI. Os clientes ADSI usam as interfaces de serviço de Active Directory bem definidas no lugar das chamadas de API específicas da rede para obter acesso mais simples aos serviços para um namespace.

Active Directory interfaces de serviço estão em conformidade com o Component Object Model (COM) e oferecem suporte a recursos COM padrão.

A ADSI fornece interfaces que são compatíveis com a automação para controladores com limite de nome, como Java, Microsoft Visual Basic Development System e Visual Basic Scripting Edition (VBScript). A ADSI também pode fornecer uma interface que pode otimizar o desempenho de interfaces que não são compatíveis com a automação, para uso com ambientes de linguagem como C e C++.

A ADSI também fornece interfaces que não são de automação, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), para dar suporte ao gerenciamento de objeto de diretório e consultas.

Além disso, a ADSI fornece seu próprio provedor de OLE DB, para que qualquer cliente que já use OLE DB, incluindo aqueles que usam ActiveX Data Objects, possa consultar serviços de diretório diretamente.

Os aplicativos Web que usam Active Server páginas também podem programar o acesso aos serviços de diretório por meio de ADSI.

Os clientes ADSI podem descobrir programaticamente todos os provedores ADSI em um site e usar as mesmas interfaces para se comunicar com cada namespace. À medida que provedores adicionais são instalados, os clientes ADSI podem se comunicar, sem recompilar, com os novos namespaces também.

Este guia de programação descreve como o ADSI funciona e fornece informações para executar tarefas específicas no ADSI. Os seguintes tópicos são abordados:

-   [Associação a um objeto ADSI](binding-to-an-adsi-object.md)
-   [Criando e excluindo objetos](creating-and-deleting-objects.md)
-   [Acessando e manipulando dados com ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Usando o esquema ADSI](using-the-adsi-schema.md)
-   [Coleções e grupos](collections-and-groups.md)
-   [Enumerando objetos ADSI](enumerating-adsi-objects.md)
-   [Pesquisando Active Directory](searching-active-directory.md)
-   [Modelo de segurança ADSI](adsi-security-model.md)
-   [Extensões ADSI](adsi-extensions.md)
-   [Usando o ADSI com o Exchange](using-adsi-with-exchange.md)
-   [Interfaces do utilitário ADSI](adsi-utility-interfaces.md)
-   [Programando ADSI com Java/COM](programming-adsi-with-javacom.md)

 

 




