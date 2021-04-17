---
description: O COM (Component Object Model) é um padrão binário para escrever software de componente em um ambiente de computação distribuído.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Fazendo backup e restaurando o banco de dados de registro de classe COM+ em VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784979"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Fazendo backup e restaurando o banco de dados de registro de classe COM+ em VSS

O COM (Component Object Model) é um padrão binário para escrever software de componente em um ambiente de computação distribuído.

A implementação original do Win32 identificadores de componente armazenados (GUIDs) e outro Estado COM no registro sob **HKEY \_ classes \_ raiz \\ CLSID**.

A geração atual do Component Object Model, COM+, oferece um banco de dados independente do registro para armazenar informações de registro do componente: o banco de dados de registro da classe COM+.

O banco de dados de registro de classe COM+ dá suporte a um gravador VSS, que permite que os solicitantes cofrentem o banco de dados de registro usando os dados armazenados em um volume copiado por sombra.

Para restaurar o banco de dados de registro do COM+, um solicitante deve chamar o método [ICOMAdminCatalog:: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

Para obter mais informações sobre o gravador de banco de dados de registro do COM+, consulte [gravadores VSS in-box](in-box-vss-writers.md).

 

 
