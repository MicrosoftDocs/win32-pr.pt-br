---
title: Gravando em um arquivo
description: Gravando em um arquivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Função AVIFileWriteData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757770"
---
# <a name="writing-to-a-file"></a>Gravando em um arquivo

Você pode gravar informações suplementares em um arquivo que foi aberto com privilégios de gravação usando a função [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) . Essa função copia as informações de um buffer fornecido pelo aplicativo e a coloca em uma ou mais partes no arquivo. O bloco "INFO" é um tipo de parte de RIFF comum no qual a função armazena informações complementares. Para obter uma descrição dos arquivos RIFF e de suas partes de dados, consulte [serviços de formato de arquivo de intercâmbio de recursos](resource-interchange-file-format-services.md).

 

 




