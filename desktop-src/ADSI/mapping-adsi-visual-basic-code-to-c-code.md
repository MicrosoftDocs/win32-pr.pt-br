---
title: mapeando código de Visual Basic ADSI para código C++
description: A ADSI consiste em mais de 50 interfaces.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179203"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>mapeando código de Visual Basic ADSI para código C++

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



 

 

 




