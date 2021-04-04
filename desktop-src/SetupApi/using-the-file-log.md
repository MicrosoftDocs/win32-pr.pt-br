---
description: Antes de usar um log de arquivos, você deve chamar SetupInitializeFileLog para abri-lo ou criá-lo. Ao chamar essa função, você pode especificar sinalizadores para criar ou substituir um log de arquivo, abrir o log do sistema ou abrir um log de arquivo como somente leitura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Usando o log de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922979"
---
# <a name="using-the-file-log"></a>Usando o log de arquivos

Antes de usar um log de arquivos, você deve chamar [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) para abri-lo ou criá-lo. Ao chamar essa função, você pode especificar sinalizadores para criar ou substituir um log de arquivo, abrir o log do sistema ou abrir um log de arquivo como somente leitura.

Depois que o [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) retorna um identificador para um log de arquivo, você pode adicionar uma entrada chamando [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), excluir uma entrada chamando [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)ou recuperar informações sobre um arquivo específico em um log de arquivos chamando [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).

Quando o log de arquivo não for mais necessário, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) deverá ser chamado para liberar os recursos alocados durante a chamada para [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).

 

 



