---
description: As funções a seguir permitem que você enumere recursos protegidos.
ms.assetid: 6806c320-6071-4075-9003-2469089a9cc4
title: Funções de WRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966e25d0c9c78e384c38098b43826f1e6342c9b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922787"
---
# <a name="wrp-functions"></a><span data-ttu-id="7393d-103">Funções de WRP</span><span class="sxs-lookup"><span data-stu-id="7393d-103">WRP Functions</span></span>

<span data-ttu-id="7393d-104">As funções a seguir permitem que você enumere recursos protegidos.</span><span class="sxs-lookup"><span data-stu-id="7393d-104">The following functions allow you to enumerate protected resources.</span></span>



| <span data-ttu-id="7393d-105">Função</span><span class="sxs-lookup"><span data-stu-id="7393d-105">Function</span></span>                                         | <span data-ttu-id="7393d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7393d-106">Description</span></span>                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="7393d-107">**SfcIsFileProtected**</span><span class="sxs-lookup"><span data-stu-id="7393d-107">**SfcIsFileProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) | <span data-ttu-id="7393d-108">Determina se o arquivo especificado está protegido.</span><span class="sxs-lookup"><span data-stu-id="7393d-108">Determines whether the specified file is protected.</span></span>         |
| [<span data-ttu-id="7393d-109">**SfcIsKeyProtected**</span><span class="sxs-lookup"><span data-stu-id="7393d-109">**SfcIsKeyProtected**</span></span>](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)   | <span data-ttu-id="7393d-110">Determina se a chave do Registro especificada está protegida.</span><span class="sxs-lookup"><span data-stu-id="7393d-110">Determines whether the specified registry key is protected.</span></span> |



 

<span data-ttu-id="7393d-111">Se estiver disponível para o sistema operacional, as funções nesta tabela devem ser usadas em vez das funções preteridas: [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) e [**SfcGetFiles**](sfcgetfiles.md).</span><span class="sxs-lookup"><span data-stu-id="7393d-111">If available for the operating system, the functions in this table should be used rather than the deprecated functions: [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) and [**SfcGetFiles**](sfcgetfiles.md).</span></span>

 

 



