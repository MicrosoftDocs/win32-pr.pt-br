---
title: Sinalizadores de criação de armazenamento
description: Os sinalizadores de criação de armazenamento especificam o que o deve fazer se um objeto de armazenamento, fluxo ou LockBytes existente tiver o mesmo nome que um novo objeto de armazenamento ou de fluxo que você está criando.
ms.assetid: 5e079716-9f68-4f1d-9c76-9199e32d78ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0532e8dd817a7f442c26490cbdd37bf3cb34d0ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291824"
---
# <a name="storage-creation-flags"></a><span data-ttu-id="56cd0-103">Sinalizadores de criação de armazenamento</span><span class="sxs-lookup"><span data-stu-id="56cd0-103">Storage Creation Flags</span></span>

<span data-ttu-id="56cd0-104">Os sinalizadores de criação de armazenamento especificam o que o deve fazer se um objeto de armazenamento, fluxo ou LockBytes existente tiver o mesmo nome que um novo objeto de armazenamento ou de fluxo que você está criando.</span><span class="sxs-lookup"><span data-stu-id="56cd0-104">Storage creation flags specify what COM should do if an existing storage, stream, or lockbytes object has the same name as a new storage or stream object that you are creating.</span></span> <span data-ttu-id="56cd0-105">O padrão é retornar uma mensagem de erro e não criar o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="56cd0-105">The default is to return an error message and not create the new object.</span></span> <span data-ttu-id="56cd0-106">Você pode usar apenas um desses sinalizadores em uma determinada chamada de criação.</span><span class="sxs-lookup"><span data-stu-id="56cd0-106">You can use only one of these flags in a given creation call.</span></span>

 

 




