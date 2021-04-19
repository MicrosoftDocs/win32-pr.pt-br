---
title: Mapeando código de Visual Basic ADSI para código C++
description: A ADSI consiste em mais de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811233"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Mapeando código de Visual Basic ADSI para código C++

A ADSI consiste em mais de 50 interfaces. A maioria das operações de diretório pode ser concluída usando apenas cinco interfaces. Eles são:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

A tabela a seguir lista os mapeamentos do código ADSI VB/VBS para o código C++. Lembre-se de que essa não é uma lista completa.



| Código VBS                           | Código VC                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = AdsGetObject ()                                                   |
| obj. Put obj. Obtenha o obj. Primária         | IADs ou IDirectoryObject                                              |
| obj. Criar obj. Excluir obj. MoveHere | IADsContainer                                                         |
| Para cada... em...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Conexão, comando, conjunto de registros     | IDirectorySearch                                                      |
| Descritor de segurança, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




