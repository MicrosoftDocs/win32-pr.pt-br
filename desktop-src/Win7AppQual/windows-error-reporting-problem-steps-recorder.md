---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Gravador de etapas de Relatório de Erros do Windows problema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663250"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="0e91e-103">Gravador de etapas de Relatório de Erros do Windows problema</span><span class="sxs-lookup"><span data-stu-id="0e91e-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0e91e-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="0e91e-104">Affected Platforms</span></span>

<span data-ttu-id="0e91e-105">**Clientes** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e91e-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="0e91e-106">**Servidores** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e91e-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="0e91e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e91e-107">Description</span></span>

<span data-ttu-id="0e91e-108">Antes do Windows 7, Relatório de Erros do Windows (WER) coletou relatórios de erros que indicaram problemas de necessidade de reparo.</span><span class="sxs-lookup"><span data-stu-id="0e91e-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="0e91e-109">Esses relatórios de erros contêm informações úteis que descrevem a natureza geral de um problema, mas não informações suficientes para determinar sua causa raiz.</span><span class="sxs-lookup"><span data-stu-id="0e91e-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="0e91e-110">Para isso, os desenvolvedores precisam de uma ferramenta para reproduzir o cenário de falha/travamento para depuração.</span><span class="sxs-lookup"><span data-stu-id="0e91e-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="0e91e-111">Um novo aplicativo, o gravador de passos para problemas (PSR.exe), está sendo enviado em todas as compilações do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e91e-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="0e91e-112">Esse recurso habilita a coleta das ações executadas por um usuário ao encontrar uma falha para que os testadores e os desenvolvedores possam reproduzir a situação de análise e depuração.</span><span class="sxs-lookup"><span data-stu-id="0e91e-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="0e91e-113">Uso</span><span class="sxs-lookup"><span data-stu-id="0e91e-113">Usage</span></span>

<span data-ttu-id="0e91e-114">Atualmente, um desenvolvedor de serviço Relatório de Erros do Windows deve solicitar a habilitação de PSR para um aplicativo; As organizações de suporte da Microsoft também usam essa ferramenta durante a solução de problemas com os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="0e91e-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="0e91e-115">Os planos estão em vigor para tornar o PSR disponível no winqual (Windows Quality Online Services) após o lançamento do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e91e-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="0e91e-116">**Observação:** Com o PSR habilitado para um aplicativo, o aplicativo pode ver alguma degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="0e91e-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="0e91e-117">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="0e91e-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="0e91e-118">Relatório de Erros do Windows entrada de blog</span><span class="sxs-lookup"><span data-stu-id="0e91e-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="0e91e-119">Winqual (Windows Quality Online Services)</span><span class="sxs-lookup"><span data-stu-id="0e91e-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
