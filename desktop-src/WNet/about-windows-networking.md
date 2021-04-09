---
title: Sobre a rede do Windows
description: Os aplicativos podem usar as funções WNet para adicionar e cancelar conexões de rede e para recuperar informações sobre a configuração atual da rede.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- WNet de rede do Windows, descrito
- WNet WNet, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006124"
---
# <a name="about-windows-networking"></a><span data-ttu-id="f5e42-105">Sobre a rede do Windows</span><span class="sxs-lookup"><span data-stu-id="f5e42-105">About Windows Networking</span></span>

<span data-ttu-id="f5e42-106">Os aplicativos podem usar as funções WNet para adicionar e cancelar conexões de rede e para recuperar informações sobre a configuração atual da rede.</span><span class="sxs-lookup"><span data-stu-id="f5e42-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="f5e42-107">A figura a seguir mostra a estrutura de uma rede típica.</span><span class="sxs-lookup"><span data-stu-id="f5e42-107">The following figure shows the structure of a typical network.</span></span>

![estrutura de rede típica](images/csnet-01.png)

<span data-ttu-id="f5e42-109">Na figura anterior, a hierarquia dos recursos do Windows NT Server/Windows 2000 Server é fornecida em detalhes como o provedor de rede \# 1.</span><span class="sxs-lookup"><span data-stu-id="f5e42-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="f5e42-110">Os recursos de rede de outros provedores têm diferentes sistemas hierárquicos.</span><span class="sxs-lookup"><span data-stu-id="f5e42-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="f5e42-111">Um aplicativo não precisa de informações sobre a hierarquia antes de começar a trabalhar com uma rede.</span><span class="sxs-lookup"><span data-stu-id="f5e42-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="f5e42-112">Ele pode prosseguir da raiz de rede (ou seja, o mais alto recurso de contêiner) e recuperar informações sobre os recursos da rede, pois as informações são necessárias.</span><span class="sxs-lookup"><span data-stu-id="f5e42-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="f5e42-113">Os recursos de rede que contêm outros recursos são chamados *contêineres*.</span><span class="sxs-lookup"><span data-stu-id="f5e42-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="f5e42-114">Os recursos de contêiner estão em caixas na figura anterior.</span><span class="sxs-lookup"><span data-stu-id="f5e42-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="f5e42-115">Os recursos que não contêm outros recursos são chamados de *objetos*.</span><span class="sxs-lookup"><span data-stu-id="f5e42-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="f5e42-116">Na figura anterior, o SharePoint \# 1 e o SharePoint \# 2 são objetos.</span><span class="sxs-lookup"><span data-stu-id="f5e42-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="f5e42-117">Um *SharePoint* é um objeto que pode ser acessado pela rede.</span><span class="sxs-lookup"><span data-stu-id="f5e42-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="f5e42-118">Exemplos de SharePoints incluem impressoras e diretórios compartilhados.</span><span class="sxs-lookup"><span data-stu-id="f5e42-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




