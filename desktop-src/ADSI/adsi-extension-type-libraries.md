---
title: Bibliotecas de tipos de extensão ADSI
description: As bibliotecas de tipos para extensões não são mescladas.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- Bibliotecas de tipos de extensão ADSI ADSI
- extensões ADSI, bibliotecas de tipo de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2390f587d5ce0d18e6e96aaf993115bb523feb340bf2becf60ceb2cff81d952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180826"
---
# <a name="adsi-extension-type-libraries"></a>Bibliotecas de tipos de extensão ADSI

As bibliotecas de tipos para extensões não são mescladas. Os clientes ADSI devem incluir especificamente a biblioteca de tipos para cada extensão. A biblioteca de tipos é necessária para Visual Basic habilitar as primeiras vinculações. Os aplicativos cliente escritos em C/C++ podem chamar o **método QueryInterface** nas interfaces de extensão definidas nos arquivos de header de extensão.

 

 




