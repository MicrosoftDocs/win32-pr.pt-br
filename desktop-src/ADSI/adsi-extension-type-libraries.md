---
title: Bibliotecas de tipos de extensão ADSI
description: As bibliotecas de tipos para extensões não são mescladas.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI de bibliotecas de tipos de extensão ADSI
- ADSI de extensões, bibliotecas de tipos de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498607"
---
# <a name="adsi-extension-type-libraries"></a>Bibliotecas de tipos de extensão ADSI

As bibliotecas de tipos para extensões não são mescladas. Os clientes ADSI devem incluir especificamente a biblioteca de tipos para cada extensão. A biblioteca de tipos é necessária para Visual Basic habilitar as ligações iniciais. Os aplicativos cliente escritos em C/C++ podem chamar o método **QueryInterface** nas interfaces de extensão definidas nos arquivos de cabeçalho de extensão.

 

 




