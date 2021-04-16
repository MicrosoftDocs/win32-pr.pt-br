---
title: Usando novos tipos de dados em seu arquivo IDL
description: O arquivo de cabeçalho Basetsd. h define os novos tipos de dados necessários para gravar aplicativos que são executados em ambas as janelas de 32 e 64 bits.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Arquivo de cabeçalho Basetsd. h programação do Windows de 64 bits
- tipos de dados no arquivo IDL programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772526"
---
# <a name="using-new-data-types-in-your-idl-file"></a>Usando novos tipos de dados em seu arquivo IDL

O arquivo de cabeçalho Basetsd. h define os novos tipos de dados necessários para gravar aplicativos que são executados em ambas as janelas de 32 e 64 bits. Para usar esses tipos de dados em suas interfaces, importe Basetsd. h para o arquivo IDL. Não \# inclua o arquivo ou você terminará com várias definições no momento da compilação.

Como alternativa, você pode incluir ou importar o arquivo Basetsd. idl em seu arquivo IDL.

Para obter mais informações sobre como adicionar arquivos de cabeçalho do sistema ao arquivo IDL, consulte [Importando arquivos e bibliotecas de tipos](/windows/desktop/Midl/importing-files-and-type-libraries) e [Importando arquivos de cabeçalho do sistema](/windows/desktop/Midl/importing-system-header-files).

 

 