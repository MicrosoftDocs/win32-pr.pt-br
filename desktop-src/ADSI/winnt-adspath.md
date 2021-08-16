---
title: ADsPath do WinNT
description: Este tópico contém exemplos de cadeias de caracteres a serem usadas para o ADsPath do WinNT.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- ADSI do provedor de serviços WinNT, ADsPath do WinNT
- ADsPath ADSI, WinNT, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838366"
---
# <a name="winnt-adspath"></a>ADsPath do WinNT

A cadeia de caracteres ADsPath do provedor ADSI WinNT pode ser uma das seguintes formas:


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



O nome de domínio pode ser um nome NETBIOS ou um nome DNS.

O servidor é o nome de um servidor específico dentro do domínio.

O caminho é o caminho de no objeto, como "diserver1/printer2".

O nome do objeto é o nome de um objeto específico.

A classe de objeto é o nome de classe do objeto nomeado. Um exemplo desse uso seria "WinNT://MyServer/JeffSmith,user". A especificação de um nome de classe pode melhorar o desempenho da operação de associação.

 

 




