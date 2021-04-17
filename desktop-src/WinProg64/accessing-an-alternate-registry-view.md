---
title: Acessando uma exibição alternativa do registro
description: Por padrão, um aplicativo de 32 bits em execução no WOW64 acessa a exibição do registro de 32 bits e um aplicativo de 64 bits acessa a exibição do registro de 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- o registro exibe a programação de 64 bits do Windows
- Programação WOW64 de 64 bits do Windows, exibições do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105797650"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="46509-105">Acessando uma exibição alternativa do registro</span><span class="sxs-lookup"><span data-stu-id="46509-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="46509-106">Por padrão, um aplicativo de 32 bits em execução no WOW64 acessa a exibição do registro de 32 bits e um aplicativo de 64 bits acessa a exibição do registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46509-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="46509-107">Os sinalizadores a seguir permitem que aplicativos de 32 bits acessem chaves redirecionadas na exibição do registro de 64 bits e aplicativos de 64 bits para acessar chaves redirecionadas na exibição de registro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="46509-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="46509-108">Esses sinalizadores não têm nenhum efeito em chaves de registro compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="46509-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="46509-109">Para obter mais informações, consulte [chaves do registro afetadas pelo WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="46509-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="46509-110">Nome do sinalizador</span><span class="sxs-lookup"><span data-stu-id="46509-110">Flag name</span></span>         | <span data-ttu-id="46509-111">Valor</span><span class="sxs-lookup"><span data-stu-id="46509-111">Value</span></span>  | <span data-ttu-id="46509-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="46509-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46509-113">CHAVE \_ 64KEY de WOW64 \_</span><span class="sxs-lookup"><span data-stu-id="46509-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="46509-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="46509-114">0x0100</span></span> | <span data-ttu-id="46509-115">Acesse uma chave de 64 bits de um aplicativo de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46509-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="46509-116">CHAVE \_ 32KEY de WOW64 \_</span><span class="sxs-lookup"><span data-stu-id="46509-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="46509-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="46509-117">0x0200</span></span> | <span data-ttu-id="46509-118">Acesse uma chave de 32 bits de um aplicativo de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46509-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="46509-119">**Windows 10 no ARM:** Isso se refere à exibição do registro ARM de 32 bits para processos ARM de 32 bits e a exibição do registro do x86 de 32 bits para processos de ARM64 de 32 bits e de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46509-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="46509-120">Esses sinalizadores podem ser especificados no parâmetro *samDesired* das seguintes funções de registro:</span><span class="sxs-lookup"><span data-stu-id="46509-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="46509-121">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="46509-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="46509-122">**RegDeleteKeyEx**</span><span class="sxs-lookup"><span data-stu-id="46509-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="46509-123">**Falha em RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="46509-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="46509-124">O \_ \_ 32KEY de WOW64 de chave ou 64KEY de WOW64 de chave \_ \_ podem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="46509-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="46509-125">Se ambos os sinalizadores forem especificados, a função falhará com o parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="46509-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="46509-126">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Se ambos os sinalizadores forem especificados, o comportamento da função s será indefinido.</span><span class="sxs-lookup"><span data-stu-id="46509-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="46509-127">A função [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) não pode ser usada para acessar uma exibição de registro alternativa.</span><span class="sxs-lookup"><span data-stu-id="46509-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="46509-128">Veja a seguir as práticas recomendadas ao acessar o registro de um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="46509-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="46509-129">Depois que o aplicativo tiver acessado uma exibição alternativa do registro usando um dos sinalizadores, todas as operações subsequentes (criar, excluir ou abrir) nas chaves do registro filho deverão usar explicitamente o mesmo sinalizador.</span><span class="sxs-lookup"><span data-stu-id="46509-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="46509-130">Caso contrário, pode haver um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="46509-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="46509-131">Para enumerar com precisão todas as chaves em ambos os modos de exibição, execute a enumeração em duas passagens.</span><span class="sxs-lookup"><span data-stu-id="46509-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="46509-132">A primeira passagem deve usar um identificador aberto com um dos sinalizadores e a outra passa usar um identificador aberto com o outro sinalizador.</span><span class="sxs-lookup"><span data-stu-id="46509-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="46509-133">As chaves **Wow6432Node** e **WowAA32Node** são reservadas.</span><span class="sxs-lookup"><span data-stu-id="46509-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="46509-134">Para compatibilidade, os aplicativos não devem usar essas chaves diretamente.</span><span class="sxs-lookup"><span data-stu-id="46509-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="46509-135">Para obter informações sobre como acessar a exibição alternativa do registro por meio do WMI, consulte [solicitando dados WMI em uma plataforma de 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="46509-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46509-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46509-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46509-137">Redirecionador de registro</span><span class="sxs-lookup"><span data-stu-id="46509-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="46509-138">Reflexão do registro</span><span class="sxs-lookup"><span data-stu-id="46509-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

