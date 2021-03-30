---
title: Instalando o provedor
description: O procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nomes de domínio, provedor WMI, instalando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635284"
---
# <a name="installing-the-provider"></a><span data-ttu-id="ef4ac-104">Instalando o provedor</span><span class="sxs-lookup"><span data-stu-id="ef4ac-104">Installing the Provider</span></span>

<span data-ttu-id="ef4ac-105">O procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que está instalado.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="ef4ac-106">O procedimento a seguir descreve como instalar e configurar o provedor WMI de DNS no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="ef4ac-107">Para obter o provedor WMI de DNS para o Windows 2000, baixe o seguinte arquivo:</span><span class="sxs-lookup"><span data-stu-id="ef4ac-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="ef4ac-108">**AVISO:** Os arquivos do provedor WMI do DNS não são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="ef4ac-109">Os servidores DNS do Windows 2000 exigem arquivos diferentes e um procedimento diferente dos servidores DNS do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="ef4ac-110">O procedimento para cada um é fornecido.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-110">The procedure for each is provided.</span></span>

<span data-ttu-id="ef4ac-111">**Para instalar o provedor WMI de DNS no Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ef4ac-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="ef4ac-112">Obtenha o provedor WMI do DNS para Windows 2000 do Windows 2000 Server Resource Kit ou baixe o arquivo, Dnsprov.zip, de: ftp://ftp.microsoft.com/reskit/win2000/</span><span class="sxs-lookup"><span data-stu-id="ef4ac-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="ef4ac-113">Copie o provedor WMI de DNS (Dnsprov.dll) e os arquivos Dnsschema. MOF para o diretório system32 do webprovider <winntdir> \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="ef4ac-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="ef4ac-114">Compile o arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-114">Compile the MOF file.</span></span> <span data-ttu-id="ef4ac-115">Isso personaliza o esquema para corresponder ao servidor.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="ef4ac-116">**Mofcomp dnsschema. mof**</span><span class="sxs-lookup"><span data-stu-id="ef4ac-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="ef4ac-117">Registre a DLL no servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="ef4ac-118">**dnsprov.dllregsvr32**</span><span class="sxs-lookup"><span data-stu-id="ef4ac-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="ef4ac-119">Os scripts ou programas que usam o provedor WMI de DNS para gerenciar servidores DNS podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="ef4ac-120">Os scripts ou programas podem ser executados por meio do servidor DNS ou de um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="ef4ac-121">O SDK do WMI não é necessário para executar o provedor WMI de DNS, mas ele contém muitas ferramentas úteis.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="ef4ac-122">O provedor WMI de DNS deve ser instalado em qualquer servidor DNS a ser gerenciado; os scripts DNS, no entanto, podem ser executados no servidor DNS ou em um host remoto.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="ef4ac-123">**Para instalar o provedor WMI de DNS no Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ef4ac-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="ef4ac-124">Para sistemas operacionais Windows Server 2003, o provedor WMI de DNS é automaticamente instalado e registrado, e seu arquivo MOF é compilado quando o serviço do servidor DNS é instalado.</span><span class="sxs-lookup"><span data-stu-id="ef4ac-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




