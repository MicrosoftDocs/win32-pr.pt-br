---
description: A interface de provedor de suporte de segurança (SSPI) permite que um aplicativo use vários modelos de segurança disponíveis em um computador ou rede sem alterar a interface para o sistema de segurança.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modelo SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370567"
---
# <a name="sspi-model"></a><span data-ttu-id="35a63-103">Modelo SSPI</span><span class="sxs-lookup"><span data-stu-id="35a63-103">SSPI Model</span></span>

<span data-ttu-id="35a63-104">A [*interface de provedor de suporte de segurança*](../secgloss/s-gly.md) (SSPI) permite que um aplicativo use vários modelos de segurança disponíveis em um computador ou rede sem alterar a interface para o sistema de segurança.</span><span class="sxs-lookup"><span data-stu-id="35a63-104">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) allows an application to use various security models available on a computer or network without changing the interface to the security system.</span></span> <span data-ttu-id="35a63-105">O SSPI não estabelece [*credenciais*](../secgloss/c-gly.md) de logon porque isso geralmente é uma operação privilegiada tratada pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="35a63-105">SSPI does not establish logon [*credentials*](../secgloss/c-gly.md) because that is generally a privileged operation handled by the operating system.</span></span>

<span data-ttu-id="35a63-106">Um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) está contido em uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ) que implementa o SSPI, tornando um ou mais [*pacotes de segurança*](../secgloss/s-gly.md) disponíveis para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="35a63-106">A [*security support provider*](../secgloss/s-gly.md) (SSP) is contained in a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements SSPI by making one or more [*security packages*](../secgloss/s-gly.md) available to applications.</span></span> <span data-ttu-id="35a63-107">Cada pacote de segurança fornece mapeamentos entre as chamadas de função SSPI de um aplicativo e as funções de um modelo de segurança real.</span><span class="sxs-lookup"><span data-stu-id="35a63-107">Each security package provides mappings between the SSPI function calls of an application and the functions of an actual security model.</span></span> <span data-ttu-id="35a63-108">Os pacotes de segurança dão suporte a [*protocolos de segurança*](../secgloss/s-gly.md) como a autenticação [*Kerberos*](../secgloss/k-gly.md) e o Gerenciador de LAN.</span><span class="sxs-lookup"><span data-stu-id="35a63-108">Security packages support [*security protocols*](../secgloss/s-gly.md) such as [*Kerberos*](../secgloss/k-gly.md) authentication and LAN Manager.</span></span>

<span data-ttu-id="35a63-109">A interface SSPI está disponível no modo kernel, bem como no modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="35a63-109">The SSPI interface is available in kernel mode as well as user mode.</span></span> <span data-ttu-id="35a63-110">Para usar a funcionalidade SSPI no modo kernel, você deve instalar o DDK do sistema de arquivos instalável do Windows.</span><span class="sxs-lookup"><span data-stu-id="35a63-110">To use SSPI functionality in kernel mode, you must install the Windows Installable File System DDK.</span></span> <span data-ttu-id="35a63-111">O modelo de chamada permanece o mesmo, mas as considerações do modo kernel são observadas nas páginas de referência de função.</span><span class="sxs-lookup"><span data-stu-id="35a63-111">The calling model remains the same, but kernel mode considerations are noted on function reference pages.</span></span> <span data-ttu-id="35a63-112">Para obter mais informações, consulte [funções SSPI](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="35a63-112">For more information, see [SSPI Functions](authentication-functions.md).</span></span>

 

 
