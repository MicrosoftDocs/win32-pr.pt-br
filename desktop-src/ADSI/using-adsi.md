---
title: Usando interfaces de serviço do Active Directory
description: O ADSI (Interfaces de Serviço do Active Directory) fornece os meios para que os aplicativos cliente de serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que fornece uma implementação ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Usando ADSI (Interfaces de Serviço do Active Directory)
- ADSI ADSI , usando
- Interfaces de serviço do Active Directory ADSI, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648846"
---
# <a name="using-active-directory-service-interfaces"></a>Usando interfaces de serviço do Active Directory

O ADSI (Interfaces de Serviço do Active Directory) fornece os meios para que os aplicativos cliente de serviços de diretório usem um conjunto de interfaces para se comunicar com qualquer namespace que fornece uma implementação ADSI. Os clientes ADSI usam as Interfaces de Serviço do Active Directory bem definidas no lugar das chamadas à API específicas de rede para obter acesso mais simples aos serviços de um namespace.

As Interfaces de Serviço do Active Directory estão em conformidade com o COM (Component Object Model) e são compatíveis com recursos COM padrão.

A ADSI fornece interfaces compatíveis com a Automação para controladores vinculados a nomes como Java, o sistema de desenvolvimento do Microsoft Visual Basic e o Visual Basic VBScript (Scripting Edition). A ADSI também pode fornecer uma interface que pode otimizar o desempenho para interfaces que não estão em conformidade com a Automação, para usar com ambientes de linguagem como C e C++.

A ADSI também fornece as interfaces de não automação, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)para dar suporte a consultas e gerenciamento de objetos de diretório.

Além disso, a ADSI fornece seu próprio provedor OLE DB, para que qualquer cliente que já use OLE DB, incluindo aqueles que usam ActiveX Data Objects, possa consultar serviços de diretório diretamente.

Aplicativos Web usando Active Server Pages também podem programar o acesso aos serviços de diretório por meio da ADSI.

Os clientes ADSI podem descobrir programaticamente todos os provedores ADSI em um site e usar as mesmas interfaces para se comunicar com cada namespace. À medida que provedores adicionais são instalados, os clientes ADSI podem se comunicar, sem recompilar, com os novos namespaces também.

Este guia de programação descreve como a ADSI funciona e fornece informações para executar tarefas específicas no ADSI. Os seguintes tópicos são abordados:

-   [Associação a um objeto ADSI](binding-to-an-adsi-object.md)
-   [Criando e excluindo objetos](creating-and-deleting-objects.md)
-   [Acessando e manipulando dados com ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Usando o esquema ADSI](using-the-adsi-schema.md)
-   [Coleções e grupos](collections-and-groups.md)
-   [Enumerando objetos ADSI](enumerating-adsi-objects.md)
-   [Pesquisando o Active Directory](searching-active-directory.md)
-   [Modelo de segurança adsi](adsi-security-model.md)
-   [Extensões ADSI](adsi-extensions.md)
-   [Usando ADSI com Exchange](using-adsi-with-exchange.md)
-   [Interfaces do Utilitário ADSI](adsi-utility-interfaces.md)
-   [Programando ADSI com Java/COM](programming-adsi-with-javacom.md)

 

 




