---
title: Usando novos tipos de dados no arquivo IDL
description: O arquivo de header Basetsd.h define os novos tipos de dados necessários para escrever aplicativos executados em 32 e 64 bits Windows.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Arquivo de Windows basetsd.h
- tipos de dados no arquivo IDL de 64 bits Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccb29ee654dc2ecc1459a4a3e8ba549e8f78a8af26a305725dbce90f469881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993916"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Usando novos tipos de dados no arquivo IDL

O arquivo de header Basetsd.h define os novos tipos de dados necessários para escrever aplicativos executados em 32 e 64 bits Windows. Para usar esses tipos de dados em suas interfaces, importe Basetsd.h para o arquivo IDL. Não inclua \# o arquivo ou você acabará com várias definições no tempo de compilação.

Como alternativa, você pode incluir ou importar o arquivo Basetsd.idl para o arquivo IDL.

Para obter mais informações sobre como adicionar arquivos de header do sistema ao arquivo IDL, consulte [Importando](/windows/desktop/Midl/importing-files-and-type-libraries) arquivos e bibliotecas de tipos e Importando arquivos [de header do sistema](/windows/desktop/Midl/importing-system-header-files).

 

 