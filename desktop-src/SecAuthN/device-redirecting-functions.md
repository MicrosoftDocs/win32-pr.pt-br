---
description: As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT. Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de uma maneira totalmente transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Funções de Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164287"
---
# <a name="device-redirecting-functions"></a><span data-ttu-id="eaf62-104">Funções de Device-Redirecting</span><span class="sxs-lookup"><span data-stu-id="eaf62-104">Device-Redirecting Functions</span></span>

<span data-ttu-id="eaf62-105">As funções de redirecionamento de dispositivo redirecionam dispositivos MS-DOS padrão, letras de unidade e portas LPT.</span><span class="sxs-lookup"><span data-stu-id="eaf62-105">The device-redirecting functions redirect standard MS-DOS devices, drive letters and LPT ports.</span></span> <span data-ttu-id="eaf62-106">Isso permite que os aplicativos em execução no sistema usem os dispositivos e acessem a rede de uma maneira totalmente transparente.</span><span class="sxs-lookup"><span data-stu-id="eaf62-106">This enables applications running on the system to use the devices and access the network in a totally transparent manner.</span></span>



| <span data-ttu-id="eaf62-107">Função</span><span class="sxs-lookup"><span data-stu-id="eaf62-107">Function</span></span>                                                         | <span data-ttu-id="eaf62-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="eaf62-108">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eaf62-109">**NPAddConnection**</span><span class="sxs-lookup"><span data-stu-id="eaf62-109">**NPAddConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | <span data-ttu-id="eaf62-110">Redireciona ou conecta um dispositivo local a um recurso de rede.</span><span class="sxs-lookup"><span data-stu-id="eaf62-110">Redirects or connects a local device to a network resource.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="eaf62-111">**NPAddConnection3**</span><span class="sxs-lookup"><span data-stu-id="eaf62-111">**NPAddConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | <span data-ttu-id="eaf62-112">Executa a mesma ação que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), mas permite que o usuário especifique qual janela deve ter qualquer caixa de diálogo e como a conexão deve ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="eaf62-112">Performs the same action as [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), but lets the user specify which window should own any dialog boxes and how the connection should be established.</span></span><br/> |
| [<span data-ttu-id="eaf62-113">**NPCancelConnection**</span><span class="sxs-lookup"><span data-stu-id="eaf62-113">**NPCancelConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | <span data-ttu-id="eaf62-114">Interrompe uma conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="eaf62-114">Breaks a network connection.</span></span> <span data-ttu-id="eaf62-115">As alterações serão lembradas se um dispositivo for desconectado, a menos que a conexão seja uma conexão sem dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eaf62-115">The changes are remembered if a device is disconnected unless the connection is a deviceless connection.</span></span><br/>                                                    |
| [<span data-ttu-id="eaf62-116">**NPGetConnection**</span><span class="sxs-lookup"><span data-stu-id="eaf62-116">**NPGetConnection**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | <span data-ttu-id="eaf62-117">Retorna informações sobre uma conexão.</span><span class="sxs-lookup"><span data-stu-id="eaf62-117">Returns information about a connection.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="eaf62-118">**NPGetConnection3**</span><span class="sxs-lookup"><span data-stu-id="eaf62-118">**NPGetConnection3**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | <span data-ttu-id="eaf62-119">Retorna informações sobre uma conexão, mesmo se a conexão estiver desconectada no momento.</span><span class="sxs-lookup"><span data-stu-id="eaf62-119">Returns information about a connection, even if the connection is currently disconnected.</span></span><br/>                                                                                                |
| [<span data-ttu-id="eaf62-120">**NPGetConnectionPerformance**</span><span class="sxs-lookup"><span data-stu-id="eaf62-120">**NPGetConnectionPerformance**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | <span data-ttu-id="eaf62-121">Retorna informações de desempenho sobre uma conexão.</span><span class="sxs-lookup"><span data-stu-id="eaf62-121">Returns performance information about a connection.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="eaf62-122">**NPGetUniversalName**</span><span class="sxs-lookup"><span data-stu-id="eaf62-122">**NPGetUniversalName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | <span data-ttu-id="eaf62-123">Retorna o nome universal ou local remoto, no formato especificado durante a chamada de função.</span><span class="sxs-lookup"><span data-stu-id="eaf62-123">Returns the remote or local universal name, in the format specified during the function call.</span></span><br/>                                                                                            |



 

 

 




