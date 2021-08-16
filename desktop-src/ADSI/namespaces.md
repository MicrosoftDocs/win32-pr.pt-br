---
title: Namespaces
description: Os objetos que residem em um determinado namespace são identificados por um nome exclusivo.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- ADSI de namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d416782f2a96ca716f6e803ad9d0b4200c82cff6ad0ad033751a89a5d2c8af1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839373"
---
# <a name="namespaces"></a>Namespaces

Os objetos que residem em um determinado namespace são identificados por um nome exclusivo. Por exemplo, os arquivos armazenados em uma unidade de disco do computador residem no namespace do sistema de arquivos. O nome exclusivo de um arquivo é baseado no local em que ele é armazenado no namespace do sistema de arquivos. Por exemplo:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Os namespaces do serviço de diretório também identificam os objetos que eles contêm por nomes exclusivos que geralmente se baseiam no local no diretório em que o objeto pode ser encontrado. Por exemplo, em um diretório X.500, um determinado objeto pode ter um nome como este:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Diferentes serviços de diretório usam formulários diferentes para nomear os objetos que eles contêm. Isso torna difícil lidar com namespaces diferentes, especialmente para desenvolvedores, considerando todos os ambientes diferentes nos quais o código pode estar em execução.

Uma meta das ADSI (Interfaces de Serviço) do Active Directory é fornecer uma estrutura de nomenplicação que permita acesso a namespaces de diferentes provedores de serviços de diretório.

A ADSI define uma convenção de nomengamento que pode identificar exclusivamente um objeto em um ambiente heterogêneo. Esses nomes são chamados de cadeias de caracteres ADsPath. As cadeias de caracteres ADsPath assumirão várias formas:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Formatos adicionais do ADsPath podem ser introduzidos por diferentes provedores ADSI (como o provedor ADSI para o servidor Serviços de Informações da Internet, que dá suporte aos ADsPaths "IIS://").

 

 




