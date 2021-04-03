---
description: Conversão manual do MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversão manual do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646349"
---
# <a name="manual-conversion-from-mts"></a><span data-ttu-id="5b812-103">Conversão manual do MTS</span><span class="sxs-lookup"><span data-stu-id="5b812-103">Manual Conversion from MTS</span></span>

<span data-ttu-id="5b812-104">Talvez você queira isolar a conversão de pacotes MTS em aplicativos COM+ para que ele esteja fora do processo de instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b812-104">You might want to isolate conversion of MTS packages to COM+ applications so that it is outside the Windows setup process.</span></span> <span data-ttu-id="5b812-105">O procedimento a seguir oferece uma abordagem alternativa:</span><span class="sxs-lookup"><span data-stu-id="5b812-105">The following procedure offers an alternate approach:</span></span>

1.  <span data-ttu-id="5b812-106">Exporte os pacotes MTS usando o recurso de exportação de pacote MTS 2,0 (resultando em um arquivo de pacote MTS e uma coleção de outros arquivos).</span><span class="sxs-lookup"><span data-stu-id="5b812-106">Export the MTS packages using the MTS 2.0 Package Export feature (resulting in an MTS package file and a collection of other files).</span></span>
2.  <span data-ttu-id="5b812-107">Exclua os pacotes MTS e atualize o Windows ou execute uma instalação limpa do Windows.</span><span class="sxs-lookup"><span data-stu-id="5b812-107">Delete the MTS packages and upgrade Windows, or perform a clean installation of Windows.</span></span>
3.  <span data-ttu-id="5b812-108">Instale os arquivos de pacote MTS (. Pak) em um sistema Windows 2000 ou posterior usando o assistente de instalação de aplicativo da ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="5b812-108">Install the MTS package (.pak) files on a Windows 2000 or later system by using the Component Services administrative tool's Application Install wizard.</span></span> <span data-ttu-id="5b812-109">Também será necessário redefinir a identidade "executar como" do aplicativo no registro do sistema em **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID \\ runas**.</span><span class="sxs-lookup"><span data-stu-id="5b812-109">You will also need to reset the application's "Run As" identity in the system registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\APPID\\RunAs**.</span></span>

> [!Note]  
> <span data-ttu-id="5b812-110">Somente o procedimento de conversão automática (por meio da instalação do Windows ou executando o utilitário MTSTOCOM) gera o arquivo de log MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="5b812-110">Only the automatic conversion procedure (through Windows setup or by running the MTSTOCOM utility) generates the MTSTOCOM log file.</span></span> <span data-ttu-id="5b812-111">Esse arquivo não é gerado ao seguir o procedimento de conversão manual.</span><span class="sxs-lookup"><span data-stu-id="5b812-111">This file is not generated when following the manual conversion procedure.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b812-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b812-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b812-113">Conversão automática do MTS</span><span class="sxs-lookup"><span data-stu-id="5b812-113">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="5b812-114">Resultados e problemas de conversão de COM+</span><span class="sxs-lookup"><span data-stu-id="5b812-114">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="5b812-115">Biblioteca de administração MTS</span><span class="sxs-lookup"><span data-stu-id="5b812-115">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



