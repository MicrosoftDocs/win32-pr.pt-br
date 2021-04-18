---
description: O Windows Installer dá suporte ao anúncio de aplicativos e recursos.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Suporte de plataforma do anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105751846"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="d6c61-103">Suporte de plataforma do anúncio</span><span class="sxs-lookup"><span data-stu-id="d6c61-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="d6c61-104">O Windows Installer dá suporte ao anúncio de aplicativos e recursos.</span><span class="sxs-lookup"><span data-stu-id="d6c61-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="d6c61-105">Os seguintes recursos de anúncio estão disponíveis no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d6c61-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="d6c61-106">Atalhos e seus ícones.</span><span class="sxs-lookup"><span data-stu-id="d6c61-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="d6c61-107">Extensões e seus ícones especificados na [tabela ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="d6c61-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="d6c61-108">Verbos de shell e comando registrados sob a chave ProgId.</span><span class="sxs-lookup"><span data-stu-id="d6c61-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="d6c61-109">Contextos de CLSID e InProcHandler.</span><span class="sxs-lookup"><span data-stu-id="d6c61-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="d6c61-110">A instalação sob demanda por meio de OLE só está disponível programaticamente por meio de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) e da **função CreateObject (Visual Basic)** ou da **função GetObject (Visual Basic)**.</span><span class="sxs-lookup"><span data-stu-id="d6c61-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="d6c61-111">As informações de AppId e TypeLib são gravadas somente quando um componente anunciado é instalado.</span><span class="sxs-lookup"><span data-stu-id="d6c61-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="d6c61-112">Para dar suporte a extensões de nome de arquivo, o aplicativo deve ser publicado para Active Directory por um administrador usando Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="d6c61-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6c61-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6c61-113">Remarks</span></span>

<span data-ttu-id="d6c61-114">A instalação do produto pode não exigir uma reinicialização, mas os atalhos anunciados não funcionam até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="d6c61-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="d6c61-115">Os atalhos anunciados das instalações subsequentes funcionam sem uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="d6c61-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="d6c61-116">Para garantir que os atalhos anunciados funcionem corretamente, o autor do pacote deve agendar uma reinicialização forçada no final da instalação.</span><span class="sxs-lookup"><span data-stu-id="d6c61-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="d6c61-117">Para evitar reinicializações desnecessárias do sistema, agende uma reinicialização para ser executada somente se nenhuma versão do Windows Installer estiver instalada.</span><span class="sxs-lookup"><span data-stu-id="d6c61-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="d6c61-118">As instruções condicionais podem verificar a propriedade [**ShellAdvtSupport**](shelladvtsupport.md) e a propriedade [**Version9X**](version9x.md) .</span><span class="sxs-lookup"><span data-stu-id="d6c61-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="d6c61-119">Para obter mais informações sobre como agendar reinicializações forçadas condicionais, consulte [reinicializações do sistema](system-reboots.md) e [uso de propriedades em instruções condicionais](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="d6c61-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
