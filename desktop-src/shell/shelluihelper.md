---
description: Implementado pelo shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell. O objeto ShellUIHelper não tem nenhuma propriedade ou evento. Os métodos são fornecidos para adicionar itens ao shell.
title: Objeto ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968192"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="69c48-105">Objeto ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="69c48-105">ShellUIHelper object</span></span>

<span data-ttu-id="69c48-106">Implementado pelo shell para ajudar o script e os desenvolvedores de Visual Basic da Microsoft a usar alguns dos recursos disponíveis no Shell.</span><span class="sxs-lookup"><span data-stu-id="69c48-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="69c48-107">O objeto **ShellUIHelper** não tem nenhuma propriedade ou evento.</span><span class="sxs-lookup"><span data-stu-id="69c48-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="69c48-108">Os métodos são fornecidos para adicionar itens ao shell.</span><span class="sxs-lookup"><span data-stu-id="69c48-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="69c48-109">Membros</span><span class="sxs-lookup"><span data-stu-id="69c48-109">Members</span></span>

<span data-ttu-id="69c48-110">O objeto **ShellUIHelper** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="69c48-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="69c48-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="69c48-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="69c48-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="69c48-112">Methods</span></span>

<span data-ttu-id="69c48-113">O objeto **ShellUIHelper** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="69c48-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="69c48-114">Método</span><span class="sxs-lookup"><span data-stu-id="69c48-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="69c48-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="69c48-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="69c48-116"><a href="shelluihelper-addchannel.md"><strong>Addchannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="69c48-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69c48-117">Adiciona um novo canal à lista de canais no menu <strong>favoritos</strong> do Internet Explorer e à barra de <strong>canais</strong> na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="69c48-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="69c48-118">Não há mais suporte para esse método no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="69c48-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="69c48-119">Nesse sistema operacional, ele retorna E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="69c48-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="69c48-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="69c48-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69c48-121">Adiciona um item à área de trabalho ativa.</span><span class="sxs-lookup"><span data-stu-id="69c48-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="69c48-122"><a href="shelluihelper-addfavorite.md"><strong>Addfavorito</strong></a></span><span class="sxs-lookup"><span data-stu-id="69c48-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69c48-123">Exibe a interface do usuário padrão para criar um item favorito.</span><span class="sxs-lookup"><span data-stu-id="69c48-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="69c48-124">A interface do usuário é inicializada para os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="69c48-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="69c48-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="69c48-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="69c48-126">Indica se uma URL especificada é assinada.</span><span class="sxs-lookup"><span data-stu-id="69c48-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="69c48-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69c48-127">Requirements</span></span>



| <span data-ttu-id="69c48-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c48-128">Requirement</span></span> | <span data-ttu-id="69c48-129">Valor</span><span class="sxs-lookup"><span data-stu-id="69c48-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c48-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69c48-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69c48-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="69c48-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="69c48-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69c48-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69c48-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="69c48-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="69c48-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="69c48-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c48-135"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69c48-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="69c48-136">DLL</span><span class="sxs-lookup"><span data-stu-id="69c48-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69c48-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="69c48-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




