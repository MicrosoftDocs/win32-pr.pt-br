---
description: A função DuplicateHandle cria um identificador duplicado que pode ser usado por outro processo especificado.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicação de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011354"
---
# <a name="object-duplication"></a>Duplicação de objeto

A função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) cria um identificador duplicado que pode ser usado por outro processo especificado. Esse método de compartilhamento de identificadores de objeto é mais complexo do que usar objetos nomeados ou herança. Ele requer a comunicação entre o processo de criação e o processo no qual o identificador está duplicado. As informações necessárias (o valor do identificador e o identificador do processo) podem ser comunicadas por qualquer um dos métodos de comunicação entre processos, como pipes nomeados ou memória compartilhada nomeada.

 

 
