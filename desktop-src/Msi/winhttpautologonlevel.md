---
description: A política de logon automático (logon automático) determina quando é aceitável que o WinHTTP inclua as credenciais padrão em uma solicitação para o servidor.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828856"
---
# <a name="winhttpautologonlevel"></a><span data-ttu-id="405b8-103">WinHttpAutoLogonLevel</span><span class="sxs-lookup"><span data-stu-id="405b8-103">WinHttpAutoLogonLevel</span></span>

<span data-ttu-id="405b8-104">A política de logon automático (logon automático) determina quando é aceitável que o *WinHTTP* inclua as credenciais padrão em uma solicitação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="405b8-104">The automatic logon (auto-logon) policy determines when it is acceptable for *WinHTTP* to include the default credentials in a request to the server.</span></span>

<span data-ttu-id="405b8-105">Você pode definir esse valor como **L** para **o nível de segurança do WinHTTP \_ AutoLogon \_ \_ \_ baixo**, definir como **M** para o nível de segurança do **WinHTTP \_ AutoLogon \_ \_ \_ Medium** e definir como **H** para o nível de **segurança do WinHTTP \_ logon automático \_ \_ \_ alto**.</span><span class="sxs-lookup"><span data-stu-id="405b8-105">You can set this value to **L** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW**, set to **M** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**, and set to **H** for **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH**.</span></span> <span data-ttu-id="405b8-106">O nível padrão é o **nível de segurança do WinHTTP com \_ logon automático \_ \_ \_ médio**.</span><span class="sxs-lookup"><span data-stu-id="405b8-106">The default level is **WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM**.</span></span> <span data-ttu-id="405b8-107">Para obter mais informações sobre a política de logon automático, consulte a seção para [autenticação no WinHTTP](../winhttp/authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="405b8-107">For more information about automatic logon policy, see the section for [Authentication in WinHTTP](../winhttp/authentication-in-winhttp.md).</span></span>

<span data-ttu-id="405b8-108">**Windows 8 e Windows Server 2012:** Essa política requer Windows Installer em execução no Windows 8 ou no Windows Server 2012 e não está disponível em todas as versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="405b8-108">**Windows 8 and Windows Server 2012:** This policy requires Windows Installer running on the Windows 8 or Windows Server 2012 and is unavailable on all earlier versions of Windows.</span></span>

## <a name="registry-key"></a><span data-ttu-id="405b8-109">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="405b8-109">Registry Key</span></span>

<span data-ttu-id="405b8-110">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="405b8-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="405b8-111">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="405b8-111">Data Type</span></span>

<span data-ttu-id="405b8-112">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="405b8-112">**REG\_SZ**</span></span>

 

 
