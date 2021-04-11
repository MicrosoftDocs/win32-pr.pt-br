---
description: Microsoft Windows Installer aceita um URL (Uniform Resource Locator) como uma fonte válida para um patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Baixando e instalando um patch da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090784"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="24730-103">Baixando e instalando um patch da Internet</span><span class="sxs-lookup"><span data-stu-id="24730-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="24730-104">Microsoft Windows Installer aceita um URL (Uniform Resource Locator) como uma fonte válida para um [patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="24730-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="24730-105">Para instalar um patch localizado em um servidor Web em https://MyWeb/MyPatch.msp , use a seguinte linha de comando:</span><span class="sxs-lookup"><span data-stu-id="24730-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="24730-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="24730-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="24730-107">Para evitar resultados inesperados, não inicie um patch clicando no link na página da Web mostrando a URL do arquivo de patch.</span><span class="sxs-lookup"><span data-stu-id="24730-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="24730-108">Você também pode instalar um patch usando um script como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="24730-108">You can also install a patch by using a script like the following:</span></span>


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="24730-109">Observe que, como o objeto do [**instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="24730-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="24730-110">Para obter mais informações, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="24730-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24730-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24730-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24730-112">Pacotes de patch</span><span class="sxs-lookup"><span data-stu-id="24730-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="24730-113">Criando um pacote de patch</span><span class="sxs-lookup"><span data-stu-id="24730-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="24730-114">Aplicação de patch em aplicativos personalizados</span><span class="sxs-lookup"><span data-stu-id="24730-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="24730-115">Baixando uma instalação da Internet</span><span class="sxs-lookup"><span data-stu-id="24730-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



