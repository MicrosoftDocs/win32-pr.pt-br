---
description: Além de enfileirar as operações de arquivo individualmente, você também pode enfileirar todos os arquivos listados em uma seção INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Enfileirando uma seção INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c419f23fe48057eec382c83b4da5e219114c186a9b7bc07c04fc5d7088b17e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964953"
---
# <a name="queuing-an-inf-section"></a>Enfileirando uma seção INF

Além de enfileirar as operações de arquivo individualmente, você também pode enfileirar todos os arquivos listados em uma seção INF.

Você pode colocar em fila todos os arquivos listados em uma seção **copiar arquivos** de um arquivo inf chamando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Para que essa função seja bem-sucedida, a seção **copiar arquivos** deve estar no formato adequado e o arquivo inf, ou um de seus arquivos anexados, deve conter as seções **SourceDisksFiles** e **SourceDisksNames** .

Da mesma forma, se você quiser excluir todos os arquivos especificados em uma seção **Excluir arquivos** de um arquivo inf, poderá chamar [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Para renomear todos os arquivos em uma seção **renomear arquivos** de um arquivo inf, use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



