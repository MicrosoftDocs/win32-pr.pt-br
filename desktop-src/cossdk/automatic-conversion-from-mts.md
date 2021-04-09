---
description: Conversão automática do MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversão automática do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089379"
---
# <a name="automatic-conversion-from-mts"></a><span data-ttu-id="435ef-103">Conversão automática do MTS</span><span class="sxs-lookup"><span data-stu-id="435ef-103">Automatic Conversion from MTS</span></span>

<span data-ttu-id="435ef-104">A conversão automática ocorre em duas etapas, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="435ef-104">Automatic conversion occurs in two steps, as follows:</span></span>

1.  <span data-ttu-id="435ef-105">Durante a instalação do Windows.</span><span class="sxs-lookup"><span data-stu-id="435ef-105">During Windows setup.</span></span> <span data-ttu-id="435ef-106">A conversão é tratada pelo processo de instalação do Windows por meio do utilitário MTSTOCOM.</span><span class="sxs-lookup"><span data-stu-id="435ef-106">The conversion is handled by the Windows setup process through the MTSTOCOM utility.</span></span>
    > [!Note]  
    > <span data-ttu-id="435ef-107">Se a etapa 1 falhar, alguns ou todos os pacotes MTS podem, na verdade, ser convertidos, mas podem estar faltando determinadas propriedades.</span><span class="sxs-lookup"><span data-stu-id="435ef-107">If step 1 fails, some or all of the MTS packages may actually have been converted but may be missing certain properties.</span></span> <span data-ttu-id="435ef-108">Nesse caso, use a ferramenta administrativa serviços de componentes para verificar todos os atributos.</span><span class="sxs-lookup"><span data-stu-id="435ef-108">In this case, use the Component Services administrative tool to verify all attributes.</span></span> <span data-ttu-id="435ef-109">Os atributos do MTS ainda estarão presentes no computador (no registro do sistema em HKEY \_ computador local \_ \\ Microsoft \\ Transaction Server), mas estarão acessíveis somente por meio do utilitário regedit.exe.</span><span class="sxs-lookup"><span data-stu-id="435ef-109">The MTS attributes will still be present on the computer (in the system registry at HKEY\_LOCAL\_MACHINE\\Microsoft\\Transaction Server) but will be accessible only through the regedit.exe utility.</span></span>

     

2.  <span data-ttu-id="435ef-110">Após a última reinicialização antes da caixa de diálogo de logon do Windows ser exibida.</span><span class="sxs-lookup"><span data-stu-id="435ef-110">After the last reboot before the Windows logon dialog box is displayed.</span></span> <span data-ttu-id="435ef-111">A etapa 2 manipula as ações de conversão que exigem o acesso à rede (principalmente a criação de membros da função).</span><span class="sxs-lookup"><span data-stu-id="435ef-111">Step 2 handles those conversion actions that require network access (primarily role member creation).</span></span>
    > [!Note]  
    > <span data-ttu-id="435ef-112">Se a etapa 2 falhar (devido a falhas temporárias de rede ou controlador de domínio), será possível executar novamente o utilitário de conversão MTSTOCOM várias vezes.</span><span class="sxs-lookup"><span data-stu-id="435ef-112">If step 2 fails (due to temporary network or domain controller failures), it is possible to rerun the MTSTOCOM conversion utility any number of times.</span></span> <span data-ttu-id="435ef-113">Para fazer isso, no prompt de comando ou depois de selecionar **executar** no menu **Iniciar** , digite o seguinte: **% windir% \\ System32 \\mtstocom.exe**.</span><span class="sxs-lookup"><span data-stu-id="435ef-113">To do this, at the command prompt or after selecting **Run** from the **Start** menu, type the following: **%windir%\\system32\\mtstocom.exe**.</span></span>

     

## <a name="mtstocom-log-file"></a><span data-ttu-id="435ef-114">Arquivo de log do MTSTOCOM</span><span class="sxs-lookup"><span data-stu-id="435ef-114">MTSTOCOM Log File</span></span>

<span data-ttu-id="435ef-115">O utilitário MTSTOCOM gera um arquivo de log (mtstocom. log) no diretório do Windows.</span><span class="sxs-lookup"><span data-stu-id="435ef-115">The MTSTOCOM utility generates a log file (Mtstocom.log) in the Windows directory.</span></span> <span data-ttu-id="435ef-116">Esse arquivo de log mantém um registro da conversão de pacotes MTS em aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="435ef-116">This log file keeps a record of the conversion from MTS packages to COM+ applications.</span></span> <span data-ttu-id="435ef-117">Se houvesse erros durante o processo de conversão, é sempre uma boa ideia verificar o arquivo de log para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="435ef-117">If there were any errors during the conversion process, it is always a good idea to check the log file for further information.</span></span> <span data-ttu-id="435ef-118">O arquivo de log captura problemas comuns, como usuário ou senha inválidos.</span><span class="sxs-lookup"><span data-stu-id="435ef-118">The log file catches common problems, such as invalid user or password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="435ef-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="435ef-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435ef-120">Resultados e problemas de conversão de COM+</span><span class="sxs-lookup"><span data-stu-id="435ef-120">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="435ef-121">Conversão manual do MTS</span><span class="sxs-lookup"><span data-stu-id="435ef-121">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="435ef-122">Biblioteca de administração MTS</span><span class="sxs-lookup"><span data-stu-id="435ef-122">MTS Administration Library</span></span>](mts-administration-library.md)
</dt> </dl>

 

 



