---
title: Configurando o servidor para carregamentos
description: Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e a extensão de servidor do BITS ISAPI instalados. Para os requisitos do IIS, consulte requisitos do IIS para carregamentos do BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159353"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="f6d36-104">Configurando o servidor para carregamentos</span><span class="sxs-lookup"><span data-stu-id="f6d36-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="f6d36-105">Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e a extensão de servidor do BITS ISAPI instalados.</span><span class="sxs-lookup"><span data-stu-id="f6d36-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="f6d36-106">Para os requisitos do IIS, consulte [requisitos do IIS para carregamentos do bits](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="f6d36-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="f6d36-107">Para obter informações sobre como configurar o diretório virtual do IIS que o BITS usa para carregamentos, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6d36-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="f6d36-108">Definindo permissões em diretórios virtuais</span><span class="sxs-lookup"><span data-stu-id="f6d36-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="f6d36-109">Gravando um script para configurar o diretório virtual</span><span class="sxs-lookup"><span data-stu-id="f6d36-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="f6d36-110">Usando a interface do usuário do IIS para configurar o diretório virtual</span><span class="sxs-lookup"><span data-stu-id="f6d36-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="f6d36-111">Impedindo vários carregamentos</span><span class="sxs-lookup"><span data-stu-id="f6d36-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="f6d36-112">Práticas recomendadas de upload</span><span class="sxs-lookup"><span data-stu-id="f6d36-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="f6d36-113">Algumas instalações do IIS incluem o componente de filtragem do UrlScan.</span><span class="sxs-lookup"><span data-stu-id="f6d36-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="f6d36-114">Se o UrlScan estiver habilitado, o administrador deverá adicionar o verbo "post do BITS \_ " à lista de VERBOS http permitidos do URLScan.</span><span class="sxs-lookup"><span data-stu-id="f6d36-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="f6d36-115">Caso contrário, haverá falha nos carregamentos do cliente BITS.</span><span class="sxs-lookup"><span data-stu-id="f6d36-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="f6d36-116">Para obter mais detalhes sobre como habilitar verbos no UrlScan, consulte a documentação do UrlScan.</span><span class="sxs-lookup"><span data-stu-id="f6d36-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




