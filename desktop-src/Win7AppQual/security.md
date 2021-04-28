---
description: Segurança (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Segurança (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116224"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="4fbd4-103">Segurança (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="4fbd4-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="4fbd4-104">A partir do Windows Internet Explorer 7, o Windows Internet Explorer é executado em um contexto de segurança chamado *modo protegido* quando os usuários o executam no sistema operacional Windows Vista ou em uma versão posterior.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="4fbd4-105">Esse modo executa o Internet Explorer em uma configuração de privilégio inferior a de um aplicativo de usuário padrão, de modo que determinadas funcionalidades sejam limitadas, especialmente controles ActiveX e certos tipos de plug-ins. Para obter mais informações sobre o modo protegido no Internet Explorer e seu impacto na compatibilidade, consulte [compreendendo e trabalhando no modo protegido do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) na biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="4fbd4-106">Por padrão, o Windows Internet Explorer 8 também permite o DEP (prevenção de execução de dados), que ajuda os aplicativos a evitar a execução de código arbitrário em ataques online.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="4fbd4-107">No entanto, alguns complementos podem não usar esse recurso de segurança (por exemplo, quaisquer complementos que não foram projetados para executar apenas o código localizado na memória que foi especificamente marcado como executável, como aplicativos que são criados usando uma versão mais antiga da estrutura da ATL (ActiveX Template Library).</span><span class="sxs-lookup"><span data-stu-id="4fbd4-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="4fbd4-108">O Internet Explorer 8 também protege os usuários contra possíveis vulnerabilidades de segurança que usam scripts.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="4fbd4-109">Por exemplo, você não pode navegar de uma URL em uma zona menos confiável para uma URL em uma zona mais confiável, exceto pela interação explícita do usuário.</span><span class="sxs-lookup"><span data-stu-id="4fbd4-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="4fbd4-110">Você também não pode ocultar determinados elementos da interface do usuário do navegador (como a barra de endereços) em uma zona não confiável (Internet).</span><span class="sxs-lookup"><span data-stu-id="4fbd4-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fbd4-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fbd4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fbd4-112">Atualizações de design que afetam a compatibilidade entre navegadores</span><span class="sxs-lookup"><span data-stu-id="4fbd4-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
