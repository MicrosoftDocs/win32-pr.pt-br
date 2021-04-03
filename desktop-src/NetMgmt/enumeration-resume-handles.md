---
title: Identificadores de retomada de enumeração
description: Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância para a função. Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916301"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="5bc5d-104">Identificadores de retomada de enumeração</span><span class="sxs-lookup"><span data-stu-id="5bc5d-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="5bc5d-105">Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância para a função.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="5bc5d-106">Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="5bc5d-107">Se um **NULL** for passado para o ponteiro para o identificador de retomada, nenhum identificador será armazenado e a pesquisa de enumeração não poderá continuar.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="5bc5d-108">Isso é útil em casos em que o aplicativo não deseja enumerar todos os itens.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="5bc5d-109">Se um erro for retornado de uma chamada de enumeração, o identificador de retomada deverá ser tratado como inválido e não será usado para nenhuma chamada de enumeração subsequente.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="5bc5d-110">Quando isso ocorrer, você deve reiniciar a enumeração desde o início.</span><span class="sxs-lookup"><span data-stu-id="5bc5d-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




