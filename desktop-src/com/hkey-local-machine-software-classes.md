---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: As subchaves e os valores de registro associados \_ à \_ chave hKey local Machine classes de \\ software \\ contêm informações sobre um aplicativo que é necessário para oferecer suporte à funcionalidade com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637101"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="9684d-103">HKEY \_ local \_ Machine \\ software \\ classes</span><span class="sxs-lookup"><span data-stu-id="9684d-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="9684d-104">As subchaves e os valores de registro associados à chave **HKEY \_ local \_ Machine \\ \\ classes de software** contêm informações sobre um aplicativo que é necessário para oferecer suporte à funcionalidade com.</span><span class="sxs-lookup"><span data-stu-id="9684d-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="9684d-105">Essas informações incluem tópicos como formatos de dados com suporte, informações de compatibilidade, identificadores programáticos, DCOM e controles.</span><span class="sxs-lookup"><span data-stu-id="9684d-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="9684d-106">Subchave</span><span class="sxs-lookup"><span data-stu-id="9684d-106">Subkey</span></span>                                                                         | <span data-ttu-id="9684d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9684d-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9684d-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="9684d-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="9684d-109">Opções de configuração para aplicativos baseados em COM.</span><span class="sxs-lookup"><span data-stu-id="9684d-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="9684d-110">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="9684d-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="9684d-111">Opções de configuração para classes COM.</span><span class="sxs-lookup"><span data-stu-id="9684d-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="9684d-112">**><\_ extensão de arquivo**</span><span class="sxs-lookup"><span data-stu-id="9684d-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="9684d-113">Associa uma extensão de nome de arquivo a um ProgID.</span><span class="sxs-lookup"><span data-stu-id="9684d-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="9684d-114">**Talvez**</span><span class="sxs-lookup"><span data-stu-id="9684d-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="9684d-115">Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para corresponder padrões em vários bytes de arquivo em um arquivo não composto.</span><span class="sxs-lookup"><span data-stu-id="9684d-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="9684d-116">**Interface**</span><span class="sxs-lookup"><span data-stu-id="9684d-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="9684d-117">Associa um nome de interface a uma ID de interface (IID).</span><span class="sxs-lookup"><span data-stu-id="9684d-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="9684d-118">Identifica uma classe.</span><span class="sxs-lookup"><span data-stu-id="9684d-118">Identifies a class.</span></span> <span data-ttu-id="9684d-119">Observe que o ProgID não tem garantia de ser globalmente exclusivo, ao contrário de um CLSID.</span><span class="sxs-lookup"><span data-stu-id="9684d-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="9684d-120">**<ProgID independente de versão>**</span><span class="sxs-lookup"><span data-stu-id="9684d-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="9684d-121">Usado para determinar a versão mais recente de um aplicativo de objeto.</span><span class="sxs-lookup"><span data-stu-id="9684d-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




