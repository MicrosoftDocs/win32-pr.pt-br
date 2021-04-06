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
# <a name="object-duplication"></a><span data-ttu-id="862b9-103">Duplicação de objeto</span><span class="sxs-lookup"><span data-stu-id="862b9-103">Object Duplication</span></span>

<span data-ttu-id="862b9-104">A função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) cria um identificador duplicado que pode ser usado por outro processo especificado.</span><span class="sxs-lookup"><span data-stu-id="862b9-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="862b9-105">Esse método de compartilhamento de identificadores de objeto é mais complexo do que usar objetos nomeados ou herança.</span><span class="sxs-lookup"><span data-stu-id="862b9-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="862b9-106">Ele requer a comunicação entre o processo de criação e o processo no qual o identificador está duplicado.</span><span class="sxs-lookup"><span data-stu-id="862b9-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="862b9-107">As informações necessárias (o valor do identificador e o identificador do processo) podem ser comunicadas por qualquer um dos métodos de comunicação entre processos, como pipes nomeados ou memória compartilhada nomeada.</span><span class="sxs-lookup"><span data-stu-id="862b9-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
