---
title: RootDSE (ADSI)
description: Cada servidor de diretório tem uma entrada exclusiva chamada RootDSE. Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59176315339e7458f332e2226f880b79afa10c5afc2c5089295866f6bf93939c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770626"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI)

Cada servidor de diretório tem uma entrada exclusiva chamada **RootDSE**. Ele fornece dados sobre o servidor, como seus recursos, a versão LDAP à qual ele dá suporte e os contextos de nomenclatura que ele usa.

por exemplo, para criar um script, ou aplicativo, que possa ser executado em qualquer ambiente de domínio Windows. Você pode especificar o nome distinto, o nome do servidor ou o nome de domínio ao se conectar a Active Directory. Se você não tiver essas informações, poderá usar o objeto **RootDSE** para estabelecer uma conexão. O exemplo de código a seguir altera a descrição de domínio em qualquer domínio.


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



Ao obter o atributo **defaultNamingContext** de **RootDSE**, você pode associar ao domínio atual, por exemplo, a Fabrikam **defaultNamingContext** é DC = Fabrikam, DC = com.

Para enumerar as propriedades do **RootDSE**, use a interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) . [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) não pode ser usado para esta tarefa.

Para obter mais informações, consulte [associação sem servidor e RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).

 

 