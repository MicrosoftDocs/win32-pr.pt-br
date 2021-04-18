---
description: Windows Installer aceita um Uniform Resource Locator (URL) como uma origem válida para uma instalação.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Baixando uma instalação da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752259"
---
# <a name="downloading-an-installation-from-the-internet"></a><span data-ttu-id="379cf-103">Baixando uma instalação da Internet</span><span class="sxs-lookup"><span data-stu-id="379cf-103">Downloading an Installation from the Internet</span></span>

<span data-ttu-id="379cf-104">Windows Installer aceita um Uniform Resource Locator (URL) como uma origem válida para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="379cf-104">Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for an installation.</span></span> <span data-ttu-id="379cf-105">Windows Installer pode instalar pacotes, patches e transformações de um local de URL.</span><span class="sxs-lookup"><span data-stu-id="379cf-105">Windows Installer can install packages, patches, and transforms from a URL location.</span></span>

<span data-ttu-id="379cf-106">Se o banco de dados de instalação estiver em uma URL, o instalador baixará o banco de dados para um local de cache antes de iniciar a instalação.</span><span class="sxs-lookup"><span data-stu-id="379cf-106">If the installation database is at a URL, the installer downloads the database to a cache location before starting the installation.</span></span> <span data-ttu-id="379cf-107">O instalador também baixa os arquivos e arquivos de gabinete da origem da Internet que são apropriados para as seleções do usuário.</span><span class="sxs-lookup"><span data-stu-id="379cf-107">The installer also downloads the files and cabinet files from the Internet source that are appropriate for the user's selections.</span></span> <span data-ttu-id="379cf-108">Consulte [um exemplo de instalação de Windows Installer baseado em URL](a-url-based-windows-installer-installation-example.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="379cf-108">See [A URL-based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md) for more information.</span></span>

<span data-ttu-id="379cf-109">Por exemplo, para instalar um pacote com uma origem localizada em um servidor Web em https://server/share/package.msi , você pode usar as opções de [linha de comando](command-line-options.md) para instalar o pacote e definir propriedades [públicas](public-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="379cf-109">For example, to install a package with a source located on a web server at https://server/share/package.msi, you can use the [command line](command-line-options.md) options to install the package and set [public](public-properties.md) properties.</span></span>

<span data-ttu-id="379cf-110">msiexec/i https://server/share/package.msi *propriedade = valor*</span><span class="sxs-lookup"><span data-stu-id="379cf-110">msiexec /i https://server/share/package.msi *PROPERTY=VALUE*</span></span>

<span data-ttu-id="379cf-111">Uma linha de comando como a mostrada anteriormente deve ser passada para o instalador para iniciar uma instalação de um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="379cf-111">A command line like the one previously shown should be passed to the installer to start an installation from a web browser.</span></span> <span data-ttu-id="379cf-112">Em geral, você não deve baixar e instalar o pacote simplesmente clicando duas vezes no arquivo. msi de dentro do navegador.</span><span class="sxs-lookup"><span data-stu-id="379cf-112">In general, you should not download and install the package simply by double-clicking the .msi file from within the browser.</span></span> <span data-ttu-id="379cf-113">Isso baixa o arquivo. msi na pasta Temporary Internet Files e passa o seguinte comando para o instalador:</span><span class="sxs-lookup"><span data-stu-id="379cf-113">This downloads the .msi file to the temporary Internet files folder and passes the following command to the installer:</span></span>

<span data-ttu-id="379cf-114">**msiexec/i c: \\ \\ arquivos de Internet temporários do Windows \\package.msi**</span><span class="sxs-lookup"><span data-stu-id="379cf-114">**msiexec /i c:\\windows\\temporary internet files\\package.msi**</span></span>

<span data-ttu-id="379cf-115">A instalação falhará se o pacote exigir arquivos de origem externos ou gabinetes, pois eles não estão localizados no mesmo local que o arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="379cf-115">The installation fails if the package requires any external source files or cabinets because these are not located in the same location as the .msi file.</span></span>

<span data-ttu-id="379cf-116">Observe que, como o objeto do [**instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="379cf-116">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="379cf-117">O método [**InstallProduct**](installer-installproduct.md) pode ser usado para executar o comando anterior de um navegador como um evento de clique.</span><span class="sxs-lookup"><span data-stu-id="379cf-117">The [**InstallProduct**](installer-installproduct.md) method could be used to run the previous command from a browser as an on-click event.</span></span>


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



<span data-ttu-id="379cf-118">Observe que, como alguns servidores Web diferenciam maiúsculas de minúsculas, o campo FileName na tabela de [arquivos](file-table.md) deve corresponder ao caso dos arquivos de origem exatamente para garantir o suporte de downloads da Internet.</span><span class="sxs-lookup"><span data-stu-id="379cf-118">Note that because some web servers are case sensitive, the FileName field in the [File](file-table.md) table must match the case of the source files exactly to ensure support of Internet downloads.</span></span>

<span data-ttu-id="379cf-119">Consulte [baixar e instalar um patch da Internet](downloading-and-installing-a-patch-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="379cf-119">See [Downloading and Installing a Patch from the Internet](downloading-and-installing-a-patch-from-the-internet.md).</span></span> <span data-ttu-id="379cf-120">Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="379cf-120">For more information about securing installations and using digital certificates, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span> <span data-ttu-id="379cf-121">Para obter mais informações sobre como criar uma instalação da Web de um pacote de Windows Installer, consulte [inicialização de download da Internet](internet-download-bootstrapping.md).</span><span class="sxs-lookup"><span data-stu-id="379cf-121">For more information about how to create a web installation of a Windows Installer package, see [Internet Download Bootstrapping](internet-download-bootstrapping.md).</span></span>

## <a name="available-internet-protocols"></a><span data-ttu-id="379cf-122">Protocolos de Internet disponíveis</span><span class="sxs-lookup"><span data-stu-id="379cf-122">Available Internet Protocols</span></span>

<span data-ttu-id="379cf-123">A partir do Windows Server 2003 e do Windows XP, o instalador pode usar os protocolos HTTP, HTTPS e FILE.</span><span class="sxs-lookup"><span data-stu-id="379cf-123">Beginning with Windows Server 2003 and Windows XP, the installer can use the HTTP, HTTPS and FILE protocols.</span></span> <span data-ttu-id="379cf-124">O instalador não dá suporte aos protocolos FTP e GOPHER.</span><span class="sxs-lookup"><span data-stu-id="379cf-124">The installer does not support the FTP and GOPHER protocols.</span></span>

<span data-ttu-id="379cf-125">Windows Installer versão 2,0 pode usar os protocolos HTTP, arquivo e FTP e não pode usar os protocolos HTTPS e GOPHER.</span><span class="sxs-lookup"><span data-stu-id="379cf-125">Windows Installer version 2.0 can use the HTTP, FILE, and FTP protocols and cannot use the HTTPS and GOPHER protocols.</span></span>

 

 



