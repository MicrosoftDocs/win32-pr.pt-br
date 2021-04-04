---
title: Registrando componentes
description: Registrando componentes
ms.assetid: d7fd231b-17ec-42ad-9144-df7ed5ffb17b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d683ae419466d62d764283cfa8706981de402a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008405"
---
# <a name="registering-components"></a><span data-ttu-id="0dfc6-103">Registrando componentes</span><span class="sxs-lookup"><span data-stu-id="0dfc6-103">Registering Components</span></span>

<span data-ttu-id="0dfc6-104">Quando os seguintes tipos de aplicativos são instalados, as informações de instalação devem ser adicionadas ao registro, geralmente por meio de um programa de instalação:</span><span class="sxs-lookup"><span data-stu-id="0dfc6-104">When the following types of applications are installed, installation information must be added to the registry, usually through a setup program:</span></span>

-   <span data-ttu-id="0dfc6-105">Aplicativos de servidor</span><span class="sxs-lookup"><span data-stu-id="0dfc6-105">Server applications</span></span>
-   <span data-ttu-id="0dfc6-106">Aplicativos de contêiner/servidor</span><span class="sxs-lookup"><span data-stu-id="0dfc6-106">Container/server applications</span></span>
-   <span data-ttu-id="0dfc6-107">Aplicativos de contêiner que permitem vincular a objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="0dfc6-107">Container applications that allow linking to embedded objects</span></span>

<span data-ttu-id="0dfc6-108">Para todas as três instâncias, registre informações de biblioteca COM (DLL) e informações específicas do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0dfc6-108">For all three instances, register COM library (DLL) information and application-specific information.</span></span>

<span data-ttu-id="0dfc6-109">A DLL registra as informações de todos os seus componentes exportando [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="0dfc6-109">The DLL registers the information for all its components by exporting [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="0dfc6-110">Use as seguintes funções para registrar e cancelar o registro de um componente:</span><span class="sxs-lookup"><span data-stu-id="0dfc6-110">Use the following functions to register and unregister a component:</span></span>

-   [<span data-ttu-id="0dfc6-111">**Falha em RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-111">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)
-   [<span data-ttu-id="0dfc6-112">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-112">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="0dfc6-113">**RegSetValueEx**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-113">**RegSetValueEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regsetvalueexa)
-   [<span data-ttu-id="0dfc6-114">**RegEnumKeyEx**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-114">**RegEnumKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regenumkeyexa)
-   [<span data-ttu-id="0dfc6-115">**RegDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-115">**RegDeleteKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeya)
-   [<span data-ttu-id="0dfc6-116">**Falha RegCloseKey**</span><span class="sxs-lookup"><span data-stu-id="0dfc6-116">**RegCloseKey**</span></span>](/windows/desktop/api/winreg/nf-winreg-regclosekey)

## <a name="related-topics"></a><span data-ttu-id="0dfc6-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0dfc6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dfc6-118">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="0dfc6-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 