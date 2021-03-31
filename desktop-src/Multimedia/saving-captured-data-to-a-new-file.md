---
title: Salvando dados capturados em um novo arquivo
description: Salvando dados capturados em um novo arquivo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS mensagem
- macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635885"
---
# <a name="saving-captured-data-to-a-new-file"></a>Salvando dados capturados em um novo arquivo

Se o usuário quiser salvar os dados capturados, o aplicativo deverá salvar o conteúdo do arquivo de captura em outro arquivo usando a [**mensagem \_ \_ \_ SaveAs do arquivo do WM Cap**](wm-cap-file-saveas.md) (ou a macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ). Essa mensagem não altera o nome ou o conteúdo do arquivo de captura. Seu aplicativo deve especificar um nome para o novo arquivo porque o arquivo de captura retém seu nome de arquivo original.

Normalmente, um arquivo de captura é pré-alocado para o maior segmento de captura previsto e apenas uma parte dele pode ser usada para capturar dados. Essa mensagem copia apenas a parte do arquivo de captura que contém os dados de captura.

 

 




