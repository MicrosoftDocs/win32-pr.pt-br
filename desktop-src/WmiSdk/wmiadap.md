---
description: Wmiadap é um aplicativo que é executado no Windows que pode atualizar informações de desempenho no repositório do WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: Wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171960"
---
# <a name="wmiadap"></a><span data-ttu-id="882b1-103">Wmiadap</span><span class="sxs-lookup"><span data-stu-id="882b1-103">wmiadap</span></span>

<span data-ttu-id="882b1-104">Wmiadap é um aplicativo que é executado no Windows que pode atualizar informações de desempenho no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="882b1-104">Wmiadap is a application that runs on Windows that can update performance information in the WMI repository.</span></span> <span data-ttu-id="882b1-105">Em geral, isso permite que os desenvolvedores e os administradores de ti criem scripts que acessam informações de desempenho, como a quantidade de memória usada por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="882b1-105">Generally, this allows developers and IT Administrators to create scripts that access performance information, such as the amount of memory used by an application.</span></span> <span data-ttu-id="882b1-106">O tópico a seguir descreve a interface de linha de comando que você pode usar para controlar como o WMIAdap recupera informações.</span><span class="sxs-lookup"><span data-stu-id="882b1-106">The following topic describes the command-line interface you can use to control how wmiadap retrieves information.</span></span>

<span data-ttu-id="882b1-107">O WMIAdap é instalado com o sistema operacional na maioria dos sistemas, no diretório C: \\ Windows \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="882b1-107">Wmiadap is installed with the operating system on most systems, in the C:\\Windows\\System32\\wbem directory.</span></span> <span data-ttu-id="882b1-108">Se você estiver vendo mensagens de erro relativas a wmiadap.exe, pesquise [suporte da Microsoft](https://support.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="882b1-108">If you are seeing error messages concerning wmiadap.exe, search [Microsoft Support](https://support.microsoft.com/).</span></span> <span data-ttu-id="882b1-109">Em geral, você não deve excluir wmiadap.exe do seu sistema, a menos que seja instruído de outra forma.</span><span class="sxs-lookup"><span data-stu-id="882b1-109">Generally, you should not delete wmiadap.exe from your system, unless otherwise instructed.</span></span>

<span data-ttu-id="882b1-110">A transferência de dados das bibliotecas de desempenho e a atualização de classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) é feita pelos provedores [WmiPerfClass](wmi-providers.md) e [WMIPerfInst](wmi-providers.md) .</span><span class="sxs-lookup"><span data-stu-id="882b1-110">The transfer of data from the performance libraries and the refresh of classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) is done by the [WmiPerfClass](wmi-providers.md) and [WMIPerfInst](wmi-providers.md) providers.</span></span> <span data-ttu-id="882b1-111">O provedor WmiPerfClass atualiza as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI somente quando um novo objeto de desempenho é adicionado.</span><span class="sxs-lookup"><span data-stu-id="882b1-111">The WmiPerfClass provider updates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) only when a new performance object is added.</span></span> <span data-ttu-id="882b1-112">Você ainda pode executar o WMIAdap com a opção **/r** para analisar os drivers de Windows Driver Model para criar objetos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="882b1-112">You still can run Wmiadap with the **/r** switch to parse the Windows Driver Model drivers to create performance objects.</span></span> <span data-ttu-id="882b1-113">A opção **/f** ainda força uma atualização das classes WMI das bibliotecas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="882b1-113">The **/f** switch still forces an update of the WMI classes from the performance libraries.</span></span>

<span data-ttu-id="882b1-114">As opções a seguir estão disponíveis no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="882b1-114">The following switches are available at the command prompt.</span></span>

<span data-ttu-id="882b1-115">**WMIAdap** \[  \] /f \[ **/r**\]</span><span class="sxs-lookup"><span data-stu-id="882b1-115">**wmiadap** \[**/f**\]\[**/r**\]</span></span>

## <a name="switches"></a><span data-ttu-id="882b1-116">Comutadores</span><span class="sxs-lookup"><span data-stu-id="882b1-116">Switches</span></span>

<dl> <dt>

<span data-ttu-id="882b1-117"><span id="_f"></span><span id="_F"></span>**f**</span><span class="sxs-lookup"><span data-stu-id="882b1-117"><span id="_f"></span><span id="_F"></span>**/f**</span></span>
</dt> <dd>

<span data-ttu-id="882b1-118">Analisa todas as bibliotecas de desempenho no sistema e atualiza as classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="882b1-118">Parses all the performance libraries on the system and refreshes the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

</dd> <dt>

<span data-ttu-id="882b1-119"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="882b1-119"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="882b1-120">Analisa todos os drivers de Windows Driver Model no sistema para criar objetos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="882b1-120">Parses all the Windows Driver Model drivers on the system to create performance objects.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="882b1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="882b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882b1-122">Bibliotecas de desempenho e WMI</span><span class="sxs-lookup"><span data-stu-id="882b1-122">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="882b1-123">**winmgmt**</span><span class="sxs-lookup"><span data-stu-id="882b1-123">**winmgmt**</span></span>](winmgmt.md)
</dt> </dl>

 

 
