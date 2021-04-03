---
description: Explica como criar um pacote de segurança personalizado.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Criando pacotes de segurança personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828838"
---
# <a name="creating-custom-security-packages"></a><span data-ttu-id="06786-103">Criando pacotes de segurança personalizados</span><span class="sxs-lookup"><span data-stu-id="06786-103">Creating Custom Security Packages</span></span>

## <a name="ssp-security-packages"></a><span data-ttu-id="06786-104">Pacotes de segurança do SSP</span><span class="sxs-lookup"><span data-stu-id="06786-104">SSP Security Packages</span></span>

<span data-ttu-id="06786-105">Se um pacote de segurança do SSP (provedor de suporte de segurança) personalizado for usado exclusivamente para o suporte de segurança de cliente/servidor, ele poderá implementar a [interface do provedor de suporte de segurança](sspi.md)da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="06786-105">If a custom security support provider (SSP) security package will be used exclusively for client/server security support it can implement the Microsoft [Security Support Provider Interface](sspi.md).</span></span>

<span data-ttu-id="06786-106">O exemplo de SampSSP fornecido com o SDK (Software Development Kit) da plataforma contém uma implementação de pacote de segurança do SSP de exemplo.</span><span class="sxs-lookup"><span data-stu-id="06786-106">The SampSSP sample shipped with the Platform Software Development Kit (SDK) contains a sample SSP security package implementation.</span></span>

## <a name="sspap-security-packages"></a><span data-ttu-id="06786-107">Pacotes de segurança do SSP/AP</span><span class="sxs-lookup"><span data-stu-id="06786-107">SSP/AP Security Packages</span></span>

<span data-ttu-id="06786-108">Os [](/windows/desktop/SecGloss/s-gly) / [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly) do provedor de suporte de segurança personalizado (SSP/APS) contêm pacotes de segurança que funcionam como pacotes de autenticação (APS) e provedores de suporte de segurança (SSPs).</span><span class="sxs-lookup"><span data-stu-id="06786-108">Custom [*security support provider*](/windows/desktop/SecGloss/s-gly)/[*authentication packages*](/windows/desktop/SecGloss/a-gly) (SSP/APs) contain security packages that function as authentication packages (APs) and security support providers (SSPs).</span></span> <span data-ttu-id="06786-109">Esses pacotes implementam APIs separadas para dar suporte a cada função.</span><span class="sxs-lookup"><span data-stu-id="06786-109">These packages implement separate APIs to support each role.</span></span>

<span data-ttu-id="06786-110">Como ele funciona como um AP, um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) SSP/PA personalizado deve fornecer implementações para todas as [funções implementadas por pacotes de autenticação](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="06786-110">Because it functions as an AP, a custom SSP/AP [*security package*](/windows/desktop/SecGloss/s-gly) must provide implementations for all of the [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="06786-111">Para fornecer suporte de segurança integrado, um pacote de segurança SSP/PA personalizado deve fornecer implementações para as [funções implementadas por SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="06786-111">To provide integrated security support, a custom SSP/AP security package must provide implementations for the [Functions implemented by SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="06786-112">As [funções LSA chamadas por SSP/APS](authentication-functions.md) descrevem as funções de suporte disponíveis para os desenvolvedores de SSP/PA que desejam interagir com a LSA.</span><span class="sxs-lookup"><span data-stu-id="06786-112">[LSA Functions Called by SSP/APs](authentication-functions.md) describes the support functions available to the SSP/AP developers that want to interact with the LSA.</span></span>

<span data-ttu-id="06786-113">Os pacotes de segurança do SSP/AP, para executar como um AP e um SSP, podem ser executados como parte do sistema operacional e como parte de um aplicativo de usuário.</span><span class="sxs-lookup"><span data-stu-id="06786-113">SSP/AP security packages, in order to perform as both an AP and an SSP, may execute as part of the operating system and as part of a user application.</span></span> <span data-ttu-id="06786-114">Esses dois modos de execução são conhecidos como modo LSA e modo de usuário, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="06786-114">These two modes of execution are known as LSA mode and user mode, respectively.</span></span> <span data-ttu-id="06786-115">Para obter detalhes sobre os pacotes de segurança personalizados no modo LSA, consulte [inicialização do modo LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="06786-115">For details about custom security packages in LSA mode see [LSA Mode Initialization](lsa-mode-initialization.md).</span></span> <span data-ttu-id="06786-116">Para obter detalhes sobre o modo de usuário, consulte [inicialização de modo de usuário](user-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="06786-116">For details about user mode, see [User Mode Initialization](user-mode-initialization.md).</span></span>

<span data-ttu-id="06786-117">Se um pacote de segurança do SSP/AP personalizado oferecer serviços para aplicativos cliente/servidor, ele deverá fornecer implementações para as funções descritas em [funções implementadas pelo SSP/APS do modo de usuário](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="06786-117">If a custom SSP/AP security package offers services for client/server applications it should provide implementations for the functions described in [Functions Implemented by User-mode SSP/APs](authentication-functions.md).</span></span> <span data-ttu-id="06786-118">As [funções LSA chamadas pelo SSP/APS do modo de usuário](authentication-functions.md) descrevem as funções de suporte disponíveis para um SSP/AP em execução em um processo de cliente ou servidor.</span><span class="sxs-lookup"><span data-stu-id="06786-118">[LSA Functions Called By User-mode SSP/APs](authentication-functions.md) describes the support functions available to an SSP/AP executing in a client or server process.</span></span>

<span data-ttu-id="06786-119">Para obter informações sobre como registrar uma DLL SSP/PA, consulte [registrando DLLs SSP/PA](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="06786-119">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06786-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06786-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06786-121">Restrições sobre o registro e a instalação de um pacote de segurança</span><span class="sxs-lookup"><span data-stu-id="06786-121">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
