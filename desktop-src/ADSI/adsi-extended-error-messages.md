---
title: Mensagens de erro estendidas ADSI
description: Este tópico contém uma lista de tópicos que explicam como trabalhar com mensagens de erro ADSI retornadas por IADs, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Mensagens de erro estendidas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004885"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="73a65-104">Mensagens de erro estendidas ADSI</span><span class="sxs-lookup"><span data-stu-id="73a65-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="73a65-105">Além dos valores **HRESULT** , vários provedores de sistema ADSI (principalmente LDAP) retornam dados de erro adicionais para operações executadas pelas seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="73a65-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="73a65-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="73a65-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="73a65-107">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="73a65-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="73a65-108">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="73a65-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="73a65-109">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="73a65-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="73a65-110">Uma parte desses dados de erro estendidos é a cadeia de caracteres enviada pelo servidor como parte do resultado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="73a65-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="73a65-111">Chame [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar essas mensagens de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="73a65-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="73a65-112">O primeiro parâmetro dessa função, *lpError*, é um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="73a65-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="73a65-113">Para um servidor Active Directory, a ADSI tenta mapear uma mensagem de erro LDAP para um código de erro Win32 apropriado e atribui o valor de código de erro do Win32 a *lpError*.</span><span class="sxs-lookup"><span data-stu-id="73a65-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="73a65-114">Falha ao resolver o mapeamento, a ADSI atribui **dados de \_ erro \_ inválidos** ao *lpError*, como faz para qualquer outro servidor de diretório.</span><span class="sxs-lookup"><span data-stu-id="73a65-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="73a65-115">Em todos os casos, a ADSI retransmite com fidelidade a cadeia de caracteres da descrição do erro do servidor para o cliente por meio de *lpErrorBuf*, o segundo parâmetro da função **ADsGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="73a65-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




