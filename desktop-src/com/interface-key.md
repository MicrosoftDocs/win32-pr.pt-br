---
title: Chave de Interface
description: Registra novas interfaces associando um nome de interface a uma ID de interface (IID). Deve haver uma subchave IID para cada nova interface.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chave do registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005877"
---
# <a name="interface-key"></a><span data-ttu-id="0f3f5-105">Chave de Interface</span><span class="sxs-lookup"><span data-stu-id="0f3f5-105">Interface Key</span></span>

<span data-ttu-id="0f3f5-106">Registra novas interfaces associando um nome de interface a uma ID de interface (IID).</span><span class="sxs-lookup"><span data-stu-id="0f3f5-106">Registers new interfaces by associating an interface name with an interface ID (IID).</span></span> <span data-ttu-id="0f3f5-107">Deve haver uma subchave IID para cada nova interface.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-107">There must be one IID subkey for each new interface.</span></span>

## <a name="registry-key"></a><span data-ttu-id="0f3f5-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="0f3f5-108">Registry Key</span></span>

<span data-ttu-id="0f3f5-109">**HKEY \_ \_Interface de \\ \\ classes de \\ software de computador local** \\ *{* IID *}*</span><span class="sxs-lookup"><span data-stu-id="0f3f5-109">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Interface**\\ *{* IID *}*</span></span>



| <span data-ttu-id="0f3f5-110">Valor do Registro</span><span class="sxs-lookup"><span data-stu-id="0f3f5-110">Registry value</span></span>                               | <span data-ttu-id="0f3f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f3f5-111">Description</span></span>                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f3f5-112">**BaseInterface**</span><span class="sxs-lookup"><span data-stu-id="0f3f5-112">**BaseInterface**</span></span>](baseinterface.md)       | <span data-ttu-id="0f3f5-113">Identifica a interface da qual a interface atual é derivada.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-113">Identifies the interface from which the current interface is derived.</span></span>                                  |
| [<span data-ttu-id="0f3f5-114">**NumMethods**</span><span class="sxs-lookup"><span data-stu-id="0f3f5-114">**NumMethods**</span></span>](nummethods.md)             | <span data-ttu-id="0f3f5-115">Contém o número de métodos na interface associada, incluindo métodos de interfaces derivadas.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-115">Contains the number of methods in the associated interface, including methods from derived interfaces.</span></span> |
| [<span data-ttu-id="0f3f5-116">**ProxyStubClsid**</span><span class="sxs-lookup"><span data-stu-id="0f3f5-116">**ProxyStubClsid**</span></span>](proxystubclsid.md)     | <span data-ttu-id="0f3f5-117">Mapeia um IID para um CLSID em DLLs de proxy de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-117">Maps an IID to a CLSID in 16-bit proxy DLLs.</span></span>                                                           |
| [<span data-ttu-id="0f3f5-118">**ProxyStubClsid32**</span><span class="sxs-lookup"><span data-stu-id="0f3f5-118">**ProxyStubClsid32**</span></span>](proxystubclsid32.md) | <span data-ttu-id="0f3f5-119">Mapeia um IID para um CLSID em DLLs de proxy de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-119">Maps an IID to a CLSID in 32-bit proxy DLLs.</span></span>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="0f3f5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f3f5-120">Remarks</span></span>

<span data-ttu-id="0f3f5-121">A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.</span><span class="sxs-lookup"><span data-stu-id="0f3f5-121">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f3f5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f3f5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f3f5-123">**Interface**</span><span class="sxs-lookup"><span data-stu-id="0f3f5-123">**Interface**</span></span>](interface.md)
</dt> </dl>

 

 




