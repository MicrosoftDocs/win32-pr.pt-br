---
title: Conectando-se ao Active Directory
description: Há vários métodos usados para acessar Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Conectando-se ao Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6afd5aa0edd8a4c4a87bae7cde6a135fc3467771eed2dbc0cb7673984040832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692004"
---
# <a name="connecting-to-active-directory"></a>Conectando-se ao Active Directory

Há vários métodos usados para acessar Active Directory. É recomendável que você use a API ADSI para acessar Active Directory. A ADSI implementa o protocolo LDAP para se comunicar com Active Directory. Os exemplos de código a seguir mostram como acessar Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Isso abre o provedor LDAP e o prepara para recuperar dados. Nenhuma conexão é estabelecida até que os dados sejam solicitados. Quando os dados são solicitados, o ADSI, com a ajuda do serviço localizador, tenta encontrar o melhor DC (controlador de domínio) para a conexão e estabelecerá uma conexão com o servidor. Esse processo é conhecido como associação sem servidor.

A ADSI também permite que você especifique o nome do servidor a ser usado para a conexão.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



Em outro cenário, você só pode saber o nome de domínio, mas não o nome do servidor específico. Novamente, a ADSI permite que você especifique o nome de domínio. no Windows 2000, o nome de domínio é representado como um nome DNS. Por exemplo, se Joe Worden, o administrador de rede, optar por se conectar usando o nome de domínio, ele poderá usar o exemplo de código a seguir.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



A ADSI se conectará a um dos controladores de domínio no domínio fabrikam.com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Associação a objetos Active Directory](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




