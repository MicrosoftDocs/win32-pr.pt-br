---
title: Configurando as DLLs de extensão
description: Na inicialização, o NPS verifica o registro para obter uma lista de DLLs de terceiros a serem chamadas.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007867"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="4aa45-103">Configurando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="4aa45-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="4aa45-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4aa45-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="4aa45-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="4aa45-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="4aa45-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="4aa45-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="4aa45-107">Na inicialização, o NPS verifica o registro para obter uma lista de DLLs de terceiros a serem chamadas.</span><span class="sxs-lookup"><span data-stu-id="4aa45-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="4aa45-108">Para configurar uma DLL de autenticação ou autorização em um servidor NPS, liste os caminhos para as DLLs em valores abaixo da seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="4aa45-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="4aa45-109">**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ Parameters\\**</span><span class="sxs-lookup"><span data-stu-id="4aa45-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="4aa45-110">Se as chaves **AuthSrv** e **Parameters** não existirem, crie-as.</span><span class="sxs-lookup"><span data-stu-id="4aa45-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="4aa45-111">O valor no qual listar as DLLs de extensão de autenticação é:</span><span class="sxs-lookup"><span data-stu-id="4aa45-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="4aa45-112">**ExtensionDLLs**</span><span class="sxs-lookup"><span data-stu-id="4aa45-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="4aa45-113">O valor no qual listar as DLLs de extensão de autorização é:</span><span class="sxs-lookup"><span data-stu-id="4aa45-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="4aa45-114">**AuthorizationDLLs**</span><span class="sxs-lookup"><span data-stu-id="4aa45-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="4aa45-115">Os valores **ExtensionDLLs** e **AuthorizationDLLs** devem ser do tipo **reg \_ multi \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="4aa45-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="4aa45-116">Esse tipo permite listar várias DLLs.</span><span class="sxs-lookup"><span data-stu-id="4aa45-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aa45-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aa45-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aa45-118">Invocando as DLLs de extensão</span><span class="sxs-lookup"><span data-stu-id="4aa45-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="4aa45-119">Atributos de identificação de usuário</span><span class="sxs-lookup"><span data-stu-id="4aa45-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 