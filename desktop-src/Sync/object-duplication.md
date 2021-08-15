---
description: A função DuplicateHandle cria um alça duplicado que pode ser usado por outro processo especificado.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicação de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886336"
---
# <a name="object-duplication"></a>Duplicação de objeto

A [**função DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) cria um alça duplicado que pode ser usado por outro processo especificado. Esse método de compartilhamento de identificador de objeto é mais complexo do que usar objetos nomeados ou herança. Ele requer comunicação entre o processo de criação e o processo no qual o handle é duplicado. As informações necessárias (o valor do identificador e o identificador do processo) podem ser comunicadas por qualquer um dos métodos de comunicação entre processos, como pipes nomeados ou memória compartilhada nomeada.

 

 
