---
title: Funções de segurança
description: As funções de segurança de gerenciamento de rede obtêm e definem descritores de segurança para raízes autônomas e baseadas em domínio do DFS.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457156"
---
# <a name="security-functions"></a><span data-ttu-id="0f83f-103">Funções de segurança</span><span class="sxs-lookup"><span data-stu-id="0f83f-103">Security Functions</span></span>

<span data-ttu-id="0f83f-104">As funções de segurança de gerenciamento de rede obtêm e definem descritores de segurança para raízes autônomas e baseadas em domínio do DFS.</span><span class="sxs-lookup"><span data-stu-id="0f83f-104">The network management security functions get and set security descriptors for DFS domain-based and stand-alone roots.</span></span>

<span data-ttu-id="0f83f-105">As funções de segurança do DFS são listadas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f83f-105">The DFS security functions are listed following.</span></span>

| <span data-ttu-id="0f83f-106">Função</span><span class="sxs-lookup"><span data-stu-id="0f83f-106">Function</span></span>                                                               | <span data-ttu-id="0f83f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f83f-107">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f83f-108">**NetDfsGetSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-108">**NetDfsGetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | <span data-ttu-id="0f83f-109">Obtém o descritor de segurança para o objeto raiz da raiz DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="0f83f-109">Obtains the security descriptor for the root object of the specified DFS root.</span></span>                                       |
| [<span data-ttu-id="0f83f-110">**NetDfsSetSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-110">**NetDfsSetSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | <span data-ttu-id="0f83f-111">Localiza o objeto raiz para a raiz DFS especificada e define o descritor de segurança fornecido nele.</span><span class="sxs-lookup"><span data-stu-id="0f83f-111">Locates the root object for the specified DFS root and sets the supplied security descriptor on it.</span></span>                  |
| [<span data-ttu-id="0f83f-112">**NetDfsGetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-112">**NetDfsGetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | <span data-ttu-id="0f83f-113">Obtém o descritor de segurança para o objeto de contêiner da raiz autônoma do DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="0f83f-113">Obtains the security descriptor for the container object of the specified DFS stand-alone root.</span></span>                      |
| [<span data-ttu-id="0f83f-114">**NetDfsSetStdContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-114">**NetDfsSetStdContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | <span data-ttu-id="0f83f-115">Localiza o objeto de contêiner para a raiz autônoma do DFS especificada e define o descritor de segurança fornecido nele.</span><span class="sxs-lookup"><span data-stu-id="0f83f-115">Locates the container object for the specified DFS stand-alone root and sets the supplied security descriptor on it.</span></span> |
| [<span data-ttu-id="0f83f-116">**NetDfsGetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-116">**NetDfsGetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | <span data-ttu-id="0f83f-117">Obtém o descritor de segurança para o objeto de contêiner da raiz de domínio do DFS especificada.</span><span class="sxs-lookup"><span data-stu-id="0f83f-117">Obtains the security descriptor for the container object of the specified DFS domain root.</span></span>                           |
| [<span data-ttu-id="0f83f-118">**NetDfsSetFtContainerSecurity**</span><span class="sxs-lookup"><span data-stu-id="0f83f-118">**NetDfsSetFtContainerSecurity**</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | <span data-ttu-id="0f83f-119">Localiza o objeto de contêiner para a raiz de domínio do DFS especificada e define o descritor de segurança fornecido nele.</span><span class="sxs-lookup"><span data-stu-id="0f83f-119">Locates the container object for the specified DFS domain root and sets the supplied security descriptor on it.</span></span>      |
