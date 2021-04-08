---
description: Explica as diferenças entre o SSP/APs e os SSPs.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs versus SSPs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922366"
---
# <a name="sspaps-vs-ssps"></a><span data-ttu-id="e6933-103">SSP/APs versus SSPs</span><span class="sxs-lookup"><span data-stu-id="e6933-103">SSP/APs vs. SSPs</span></span>

<span data-ttu-id="e6933-104">Os [*pacotes de segurança*](../secgloss/s-gly.md) são implantados em um dos seguintes tipos de DLLs (bibliotecas de vínculo dinâmico):</span><span class="sxs-lookup"><span data-stu-id="e6933-104">[*Security packages*](../secgloss/s-gly.md) are deployed in one of the following types of dynamic-link libraries (DLLs):</span></span>

-   [<span data-ttu-id="e6933-105">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="e6933-105">SSP/APs</span></span>](#sspaps-vs-ssps)
-   [<span data-ttu-id="e6933-106">SSPs</span><span class="sxs-lookup"><span data-stu-id="e6933-106">SSPs</span></span>](#sspaps-vs-ssps)

<span data-ttu-id="e6933-107">Se um pacote de segurança está em um provedor de suporte de segurança/um [*pacote de autenticação*](../secgloss/a-gly.md) (SSP/AP) ou uma DLL do SSP (provedor de [*suporte de segurança*](../secgloss/s-gly.md) ) é determinada pelos tipos de serviços de segurança que ele fornece e da extensão para a qual ele requer integração com a [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA).</span><span class="sxs-lookup"><span data-stu-id="e6933-107">Whether a security package is in a security support provider/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) or a [*security support provider*](../secgloss/s-gly.md) (SSP) DLL is determined by the types of security services it provides and the extent to which it requires integration with the [*Local Security Authority*](../secgloss/l-gly.md) (LSA).</span></span> <span data-ttu-id="e6933-108">Essas diferenças também determinam a API implementada em um pacote de segurança personalizado.</span><span class="sxs-lookup"><span data-stu-id="e6933-108">These differences also determine the API implemented in a custom security package.</span></span>

## <a name="sspaps"></a><span data-ttu-id="e6933-109">SSP/APs</span><span class="sxs-lookup"><span data-stu-id="e6933-109">SSP/APs</span></span>

<span data-ttu-id="e6933-110">Um SSP/AP é uma DLL que contém um ou mais [*pacotes de segurança*](../secgloss/s-gly.md) e pode funcionar como um SSP para aplicativos cliente/servidor e como um [pacote de autenticação](authentication-packages.md) para aplicativos de logon.</span><span class="sxs-lookup"><span data-stu-id="e6933-110">An SSP/AP is a DLL that contains one or more [*Security packages*](../secgloss/s-gly.md) and can function as an SSP for client/server applications and as an [authentication package](authentication-packages.md) for logon applications.</span></span> <span data-ttu-id="e6933-111">Para funcionar em ambas as funções, os SSP/APs são carregados no espaço de processo do LSA na inicialização do sistema e podem ser carregados em processos de aplicativos cliente/servidor também.</span><span class="sxs-lookup"><span data-stu-id="e6933-111">To function in both of these roles, SSP/APs are loaded into the LSA process space at system startup and can be loaded into client/server application processes as well.</span></span>

<span data-ttu-id="e6933-112">Os pacotes de segurança do SSP/AP personalizados devem implementar as [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md)e [funções implementadas pelo SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e6933-112">Custom SSP/AP security packages must implement both the [Functions Implemented by User-mode SSP/APs](authentication-functions.md), and [Functions Implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="e6933-113">Essas implementações de função podem fazer uso de funções de suporte de LSA para oferecer recursos avançados de segurança, como a criação de tokens, suporte a [*credenciais complementares*](../secgloss/s-gly.md) e autenticação de passagem.</span><span class="sxs-lookup"><span data-stu-id="e6933-113">These function implementations can make use of LSA support functions to offer advanced security features such as token creation, [*supplemental credentials*](../secgloss/s-gly.md) support, and pass-through authentication.</span></span>

<span data-ttu-id="e6933-114">Se um pacote de segurança do SSP/AP personalizado fornecer uma gama completa de funções de [*integridade*](../secgloss/i-gly.md) e privacidade de mensagens, ele também implementará as [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e6933-114">If a custom SSP/AP security package provides the full range of message [*integrity*](../secgloss/i-gly.md) and privacy functions, it will also implement the [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span>

## <a name="ssps"></a><span data-ttu-id="e6933-115">SSPs</span><span class="sxs-lookup"><span data-stu-id="e6933-115">SSPs</span></span>

<span data-ttu-id="e6933-116">Um SSP é uma DLL que contém um ou mais pacotes de segurança que fornecem conexão autenticada, integridade de mensagem e serviços de criptografia de mensagens a aplicativos cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="e6933-116">An SSP is a DLL that contains one or more security packages that provide authenticated connection, message integrity, and message encryption services to client/server applications.</span></span> <span data-ttu-id="e6933-117">Os SSPs implementam as funções de SSPI ( [interface do provedor de suporte de segurança](sspi.md) ).</span><span class="sxs-lookup"><span data-stu-id="e6933-117">SSPs implement [Security Support Provider Interface](sspi.md) (SSPI) functions.</span></span> <span data-ttu-id="e6933-118">Os aplicativos podem acessar os pacotes de segurança em um SSP chamando as funções SSPI diretamente.</span><span class="sxs-lookup"><span data-stu-id="e6933-118">Applications can access the security packages in an SSP by calling the SSPI functions directly.</span></span> <span data-ttu-id="e6933-119">Os SSPs são carregados nos processos de cliente e servidor; Eles não são integrados à LSA.</span><span class="sxs-lookup"><span data-stu-id="e6933-119">SSPs are loaded into the client and server processes; they are not integrated with the LSA.</span></span>

 

 
