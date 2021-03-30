---
title: Salvando conteúdo gravado
description: Salvando conteúdo gravado
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Macro MCIWndSave
- Macro MCIWndSaveDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635884"
---
# <a name="saving-recorded-content"></a>Salvando conteúdo gravado

Depois de concluir a gravação, você pode salvar o conteúdo usando a macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) ou [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) ou usando a função [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) com **MCIWndSave**. A macro **MCIWndSave** salva os dados no arquivo associado à janela MCIWnd. A macro **MCIWndSaveDialog** permite que o usuário especifique um nome de arquivo e salve os dados gravados no arquivo especificado. A função **GetSaveFileNamePreview** exibe a caixa de diálogo **salvar** como para escolher um arquivo e permite que o usuário visualize (Execute) o arquivo. Quando o nome de um arquivo existente é especificado na caixa de diálogo **salvar** como, o **GetSaveFileNamePreview** fornece um pequeno controle na caixa de diálogo para permitir que o usuário visualize o conteúdo do arquivo. Você pode salvar os dados gravados em um arquivo selecionado com **GetSaveFileNamePreview** usando **MCIWndSave**.

 

 




