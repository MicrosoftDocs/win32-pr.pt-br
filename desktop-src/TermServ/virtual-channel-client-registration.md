---
title: Registro de cliente de canal virtual
description: Você deve armazenar o nome da DLL do cliente no registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641248"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="6b8de-103">Registro de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="6b8de-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="6b8de-104">Você deve armazenar o nome da DLL do cliente no registro.</span><span class="sxs-lookup"><span data-stu-id="6b8de-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="6b8de-105">No registro, adicione uma subchave a um dos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="6b8de-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="6b8de-106">**HKEY \_ Software do \_ usuário atual** \\  \\  \\  \\  \\ **suplementos** do cliente Microsoft Terminal Server Client</span><span class="sxs-lookup"><span data-stu-id="6b8de-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="6b8de-107">**HKEY \_ \_** \\  \\ Suplementos de conexão de cliente **do Microsoft** \\ **Terminal Server Client** \\  \\  software atual</span><span class="sxs-lookup"><span data-stu-id="6b8de-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="6b8de-108">No caminho do registro, a *conexão* representa o nome de uma conexão no Gerenciador de conexões.</span><span class="sxs-lookup"><span data-stu-id="6b8de-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="6b8de-109">As entradas na chave de **\\ \\ suplementos padrão** se aplicam a todas as conexões.</span><span class="sxs-lookup"><span data-stu-id="6b8de-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="6b8de-110">As entradas na chave de **\\  \\ suplementos de conexão** aplicam-se somente à conexão identificada pela *conexão*.</span><span class="sxs-lookup"><span data-stu-id="6b8de-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="6b8de-111">As conexões podem ser criadas e gerenciadas usando o Gerenciador de conexões.</span><span class="sxs-lookup"><span data-stu-id="6b8de-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="6b8de-112">A subchave pode receber qualquer nome.</span><span class="sxs-lookup"><span data-stu-id="6b8de-112">The subkey can be given any name.</span></span> <span data-ttu-id="6b8de-113">Ele deve conter um valor de reg **\_ sz** ou **reg \_ expande \_ sz** e pode, opcionalmente, conter um valor **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6b8de-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="6b8de-114">A sintaxe do valor **reg \_ sz** ou **reg \_ expande \_ sz** é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="6b8de-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="6b8de-115">Se **Name** for um valor **reg \_ Expand \_ sz** , ele poderá conter variáveis de ambiente não expandidas que são expandidas no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6b8de-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="6b8de-116">O valor de *DllName* pode ser um caminho totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6b8de-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="6b8de-117">Se *DllName* não contiver um caminho, a estratégia de pesquisa padrão de dll será usada.</span><span class="sxs-lookup"><span data-stu-id="6b8de-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="6b8de-118">Para obter mais informações, consulte a seção comentários para [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="6b8de-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 