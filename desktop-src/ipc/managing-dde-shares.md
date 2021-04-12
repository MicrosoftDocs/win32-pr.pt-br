---
description: O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: Gerenciando compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcc8c7d2eb3983aaabd054b9b729daea176bb10
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104297839"
---
# <a name="managing-dde-shares"></a><span data-ttu-id="61cc8-103">Gerenciando compartilhamentos DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-103">Managing DDE Shares</span></span>

<span data-ttu-id="61cc8-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="61cc8-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="61cc8-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="61cc8-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="61cc8-106">O DDE de rede fornece funções que permitem excluir um compartilhamento, obter ou definir informações de compartilhamento ou enumerar compartilhamentos.</span><span class="sxs-lookup"><span data-stu-id="61cc8-106">Network DDE provides functions that allow you to delete a share, get or set share information, or enumerate shares.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61cc8-107">Tarefa</span><span class="sxs-lookup"><span data-stu-id="61cc8-107">Task</span></span></th>
<th><span data-ttu-id="61cc8-108">Procedimento</span><span class="sxs-lookup"><span data-stu-id="61cc8-108">Procedure</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61cc8-109">Excluir um compartilhamento de DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-109">Delete a DDE share</span></span></td>
<td><span data-ttu-id="61cc8-110">Use a função <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-110">Use the <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61cc8-111">Obter informações de compartilhamento de DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-111">Get DDE share information</span></span></td>
<td><span data-ttu-id="61cc8-112">Use a função <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-112">Use the <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61cc8-113">Definir informações de compartilhamento DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-113">Set DDE share information</span></span></td>
<td><span data-ttu-id="61cc8-114">Use a função <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-114">Use the <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61cc8-115">Enumerar compartilhamentos DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-115">Enumerate DDE shares</span></span></td>
<td><span data-ttu-id="61cc8-116">Use a função <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-116">Use the <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> function.</span></span> <span data-ttu-id="61cc8-117">Você também pode enumerar os compartilhamentos DDE confiáveis usando a função <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-117">You can also enumerate the trusted DDE shares by using the <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61cc8-118">Enumerar usuários conectados</span><span class="sxs-lookup"><span data-stu-id="61cc8-118">Enumerate connected users</span></span></td>
<td><span data-ttu-id="61cc8-119">Use a função <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61cc8-119">Use the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> function.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61cc8-120">Alterar o nome do compartilhamento DDE</span><span class="sxs-lookup"><span data-stu-id="61cc8-120">Change the DDE share name</span></span></td>
<td><span data-ttu-id="61cc8-121">Exclua o compartilhamento antigo e crie um novo compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="61cc8-121">Delete the old share and create a new share.</span></span>
<ol>
<li><span data-ttu-id="61cc8-122">Recupere as informações de compartilhamento usando <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="61cc8-122">Retrieve the share information using <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="61cc8-123">Remova o compartilhamento usando <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="61cc8-123">Remove the share using <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>.</span></span></li>
<li><span data-ttu-id="61cc8-124">Altere o membro <strong>lpszShareName</strong> da estrutura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> retornada por <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="61cc8-124">Change the <strong>lpszShareName</strong> member of the <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure returned by <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>.</span></span></li>
<li><span data-ttu-id="61cc8-125">Passe a estrutura <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> modificada para <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="61cc8-125">Pass the modified <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> structure to <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

