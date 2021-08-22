---
title: Enumerando grupos que contêm muitos membros
description: saiba mais sobre como enumerar grupos de Azure Active Directory que contêm muitos membros usando a recuperação incremental de dados (recuperação de intervalo).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerando grupos que contêm muitos membros Active Directory
- grupos Active Directory, enumerando grupos com muitos membros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550ec2f4a77938b26e2273d468d3f9740d637249501aa2396fef3744cd105060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695134"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Enumerando grupos que contêm muitos membros

Os membros de um grupo são armazenados em um atributo com vários valores chamado **membro**. O atributo **Member** pode conter um grande número de valores. A enumeração de membros pode ser ineficiente quando o número de valores em um atributo com vários valores se torna grande. O servidor também limitará o número máximo de valores que podem ser recuperados em uma única consulta. Isso significa que, se um grupo pode ter mais membros do que pode ser fornecido pelo servidor, a única maneira de enumerar todos os membros é usar a recuperação incremental de dados, conhecida como *recuperação de intervalo*.

A recuperação de intervalo envolve a solicitação de um número limitado de valores de atributo em uma única consulta. O número de valores solicitados deve ser menor ou igual ao número máximo de valores com suporte pelo servidor. Para reduzir o número de vezes que a consulta deve entrar em contato com o servidor, o número de valores solicitados deve ser o mais próximo possível, para esse máximo. Para permitir que um aplicativo funcione corretamente com todos os servidores, um número máximo de 1000 deve ser usado.

A versão do servidor que fornece os dados solicitados determina o número máximo de valores que podem ser recuperados em uma única consulta. A tabela a seguir lista a versão do servidor e o número máximo de valores que podem ser recuperados em uma única consulta.



| Versão do sistema operacional do servidor | Valores máximos recuperados |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1500                     |



 

Para obter mais informações sobre como recuperar intervalos de valores de atributo com ADSI, consulte [recuperação de intervalo de atributo](/windows/desktop/ADSI/attribute-range-retrieval).

Para obter mais informações sobre como recuperar intervalos de valores de atributo com [System. DirectoryServices](/dotnet/api/system.directoryservices), consulte [enumerando Membros em um grupo grande](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).

 

 