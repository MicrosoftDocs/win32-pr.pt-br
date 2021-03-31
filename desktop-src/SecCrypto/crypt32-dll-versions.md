---
description: Crypt32.dll é o módulo que implementa muitas das funções de CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versões do Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647005"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="ed0e7-103">Versões do Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="ed0e7-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="ed0e7-104">Crypt32.dll é o módulo que implementa muitas das funções de certificado e de mensagens criptográficas no CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="ed0e7-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="ed0e7-105">Crypt32.dll é um módulo que acompanha os sistemas operacionais Windows e Windows Server, mas versões diferentes dessa DLL fornecem recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="ed0e7-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="ed0e7-106">Não há API para determinar a versão do CryptoAPI que está em uso, mas você pode determinar a versão do Crypt32.dll que está em uso no momento usando as funções [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .</span><span class="sxs-lookup"><span data-stu-id="ed0e7-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="ed0e7-107">Em geral, os intervalos de versão do Crypt32.dll são mapeados para as versões do sistema operacional, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed0e7-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="ed0e7-108">No entanto, essa tabela deve ser usada como uma diretriz somente porque é possível, por meio de outros caminhos de atualização, que a versão Crypt32.dll será diferente da indicada na tabela.</span><span class="sxs-lookup"><span data-stu-id="ed0e7-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="ed0e7-109">Versão do Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="ed0e7-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="ed0e7-110">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="ed0e7-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0e7-111">*versão* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="ed0e7-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="ed0e7-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ed0e7-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="ed0e7-113">*versão* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="ed0e7-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="ed0e7-114">Windows XP com Service Pack 2 (SP2) Windows XP com Service Pack 1 (SP1) com hotfix [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="ed0e7-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="ed0e7-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed0e7-115">Windows XP</span></span><br/> |
| <span data-ttu-id="ed0e7-116">5.131.2600.0 <= *versão* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="ed0e7-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="ed0e7-117">Windows XP com SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="ed0e7-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
