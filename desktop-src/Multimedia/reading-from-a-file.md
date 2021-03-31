---
title: Lendo de um arquivo
description: Lendo de um arquivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Função AVIFileInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005935"
---
# <a name="reading-from-a-file"></a>Lendo de um arquivo

Você pode recuperar informações sobre um arquivo aberto usando a função [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) . Essa função preenche a estrutura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) com tais informações como a taxa máxima de dados, o número de fluxos no arquivo, se o arquivo usa um índice e se o arquivo está protegido por direitos autorais.

Para recuperar informações suplementares em um arquivo AVI, use a função [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) . As informações complementares são aplicáveis ao arquivo inteiro e não estão incluídas nos cabeçalhos de arquivo normais. Por exemplo, o nome da empresa ou pessoa que mantém os direitos autorais de um arquivo pode ser informações complementares. As informações suplementares não aderem a um formato específico; Ele pode ser específico do arquivo. **AVIFileReadData** retorna as informações suplementares em um buffer fornecido pelo aplicativo.

 

 




