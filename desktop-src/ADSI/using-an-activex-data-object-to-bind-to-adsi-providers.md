---
title: Usando um objeto de dados ActiveX para ligar a provedores ADSI
description: Como a ADSI também é um provedor de OLE DB, você pode usar um ADO (ActiveX Data Object) para se conectar a provedores ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ADSI do objeto de dados ActiveX
- ADSI do objeto de dados ActiveX, usando o ADO para ligar a provedores ADSI
- ADSI de provedores de serviço, usando o objeto de dados ActiveX para associar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004851"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>Usando um objeto de dados ActiveX para ligar a provedores ADSI

Como a ADSI também é um provedor de OLE DB, você pode usar um ADO (ActiveX Data Object) para se conectar a provedores ADSI. Assim como ocorre com outros provedores de ADO, para se conectar a um provedor de OLE DB, você deve criar um novo objeto de conexão e, opcionalmente, especificar as credenciais. O nome do provedor de OLE DB ADSI é **ADsDSOObject**.

Por exemplo:


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



No exemplo anterior, você está conectado em nome do usuário atual. Para especificar credenciais diferentes, use as propriedades de conexão:


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



O OLE DB ADSI define as propriedades de conexão a seguir.



| Propriedade           | Tipo de dados   | Padrão   |
|--------------------|-------------|-----------|
| "ID de usuário"          | **BSTR**    | **NULL**  |
| "Password"         | **BSTR**    | **NULL**  |
| "Criptografar senha" | **BOOLEAN** | **FALSE** |
| "Sinalizador ADSI"        | **Long**    | 0         |



 

Usando OLE DB ADO, não é possível associar a um objeto específico. No entanto, você pode consultar um objeto específico e obter um conjunto de resultados de volta. Somente os provedores ADSI que dão suporte ao [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se beneficiam de ter o ADO como um modelo de programação.

A propriedade de sinalizador ADSI é usada para especificar a opção de autenticação de associação. Essa propriedade pode ser uma combinação de sinalizadores da enumeração de enumeração de [**\_ \_ autenticação do ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .

 

 




