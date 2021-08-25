---
title: Salvando dados capturados em um novo arquivo
description: Salvando dados capturados em um novo arquivo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS mensagem
- macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f6f2f94ed1a7c7f7f8cae20b20c6fa4b5aa27e8105ab3f5dc33e60b7aff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892906"
---
# <a name="saving-captured-data-to-a-new-file"></a>Salvando dados capturados em um novo arquivo

Se o usuário quiser salvar os dados capturados, o aplicativo deverá salvar o conteúdo do arquivo de captura em outro arquivo usando a [**mensagem \_ \_ \_ SaveAs do arquivo do WM Cap**](wm-cap-file-saveas.md) (ou a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ). Essa mensagem não altera o nome ou o conteúdo do arquivo de captura. Seu aplicativo deve especificar um nome para o novo arquivo porque o arquivo de captura retém seu nome de arquivo original.

Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados. Essa mensagem copia apenas a parte do arquivo de captura que contém os dados de captura.

 

 




