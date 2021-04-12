---
title: Namespaces
description: Os objetos que residem em um namespace específico são identificados por um nome exclusivo.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- ADSI de namespaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363649"
---
# <a name="namespaces"></a>Namespaces

Os objetos que residem em um namespace específico são identificados por um nome exclusivo. Por exemplo, os arquivos armazenados em uma unidade de disco do PC residem no namespace do sistema de arquivos. O nome exclusivo de um arquivo é baseado em onde ele é armazenado no namespace do sistema de arquivos. Por exemplo:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Os namespaces do serviço de diretório também identificam os objetos que eles contêm por nomes exclusivos que geralmente são baseados no local no diretório onde o objeto pode ser encontrado. Por exemplo, em um diretório X. 500, um determinado objeto pode ter um nome como este:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Serviços de diretório diferentes usam formulários diferentes para nomear os objetos que eles contêm. Isso torna o tratamento de diferentes namespaces desafiador, especialmente para desenvolvedores, considerando todos os diferentes ambientes nos quais o código pode estar em execução.

Uma meta do ADSI (Active Directory Service Interfaces) é fornecer uma estrutura de nomenclatura que permita o acesso a namespaces de diferentes provedores de serviço de diretório.

A ADSI define uma Convenção de nomenclatura que pode identificar exclusivamente um objeto em um ambiente heterogêneo. Esses nomes são chamados de cadeias de caracteres ADsPath. As cadeias de caracteres ADsPath assumem várias formas:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Formatos ADsPath adicionais podem ser introduzidos por diferentes provedores ADSI (como o provedor ADSI para o Serviços de Informações da Internet Server, que dá suporte ao ADsPaths "IIS://").

 

 




