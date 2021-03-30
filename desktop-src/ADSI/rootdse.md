---
title: RootDSE (ADSI)
description: Cada servidor de diretório tem uma entrada exclusiva chamada RootDSE. Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641835"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Cada servidor de diretório tem uma entrada exclusiva chamada **RootDSE**. Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.

Por exemplo, para criar um script, ou aplicativo, que possa ser executado em qualquer ambiente de domínio do Windows. Você pode especificar o nome distinto, o nome do servidor ou o nome de domínio ao se conectar a Active Directory. Se você não tiver essas informações, poderá usar o objeto **RootDSE** para estabelecer uma conexão. O exemplo de código a seguir altera a descrição de domínio em qualquer domínio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Ao obter o atributo **defaultNamingContext** de **RootDSE**, você pode associar ao domínio atual, por exemplo, a Fabrikam **defaultNamingContext** é DC = Fabrikam, DC = com.

Para enumerar as propriedades do **RootDSE**, use a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) não pode ser usado para esta tarefa.

Para obter mais informações, consulte [associação sem servidor e RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 