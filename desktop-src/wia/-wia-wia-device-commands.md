---
description: As constantes a seguir formam o conjunto de comandos válidos do dispositivo de hardware WIA (Windows Image Acquisition).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandos do dispositivo WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827163"
---
# <a name="wia-device-commands"></a><span data-ttu-id="c453f-103">Comandos do dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="c453f-103">WIA Device Commands</span></span>

<span data-ttu-id="c453f-104">As constantes a seguir formam o conjunto de comandos válidos do dispositivo de hardware WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="c453f-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c453f-105">Constante</span><span class="sxs-lookup"><span data-stu-id="c453f-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c453f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c453f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="c453f-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-108">Faz com que o minidriver do dispositivo sincronize itens em cache com o dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="c453f-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="c453f-109">Se o dispositivo der suporte ao método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , emitir esse comando fará com que o minidriver descarte os resultados da análise e redefina o item para seu estado inicial.</span><span class="sxs-lookup"><span data-stu-id="c453f-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="c453f-110">Todos os drivers devem dar suporte a esse comando.</span><span class="sxs-lookup"><span data-stu-id="c453f-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="c453f-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-112">Faz com que um dispositivo WIA adquira uma imagem.</span><span class="sxs-lookup"><span data-stu-id="c453f-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="c453f-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-114">Informa ao dispositivo para excluir todos os itens que podem ser excluídos da árvore de objetos <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> que representam o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c453f-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="c453f-115">A exclusão do item é impedida pela definição das propriedades do item.</span><span class="sxs-lookup"><span data-stu-id="c453f-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="c453f-116">Para obter detalhes, consulte <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">atributos de propriedade</a>.</span><span class="sxs-lookup"><span data-stu-id="c453f-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="c453f-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-118">Usado para scanners de documento.</span><span class="sxs-lookup"><span data-stu-id="c453f-118">Used for document scanners.</span></span> <span data-ttu-id="c453f-119">Faz com que o verificador carregue a próxima página em seu manipulador de documentos.</span><span class="sxs-lookup"><span data-stu-id="c453f-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="c453f-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-121">Usado para scanners de documento.</span><span class="sxs-lookup"><span data-stu-id="c453f-121">Used for document scanners.</span></span> <span data-ttu-id="c453f-122">Instrui o dispositivo a descarregar todas as páginas restantes em seu manipulador de documentos.</span><span class="sxs-lookup"><span data-stu-id="c453f-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="c453f-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-124">Usado para scanners de documento que têm um alimentador de página.</span><span class="sxs-lookup"><span data-stu-id="c453f-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="c453f-125">Instrui o dispositivo a iniciar o motor do alimentador.</span><span class="sxs-lookup"><span data-stu-id="c453f-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="c453f-126">Esse recurso está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c453f-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c453f-127">O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="c453f-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="c453f-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-129">Usado para scanners de documento que têm um alimentador de página.</span><span class="sxs-lookup"><span data-stu-id="c453f-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="c453f-130">Instrui o dispositivo a parar o motor do alimentador.</span><span class="sxs-lookup"><span data-stu-id="c453f-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="c453f-131">Esse recurso está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c453f-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c453f-132">O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="c453f-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="c453f-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c453f-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c453f-134">Usado para scanners de documento que têm um alimentador de página.</span><span class="sxs-lookup"><span data-stu-id="c453f-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="c453f-135">Instrui o dispositivo a pausar o motor do alimentador.</span><span class="sxs-lookup"><span data-stu-id="c453f-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="c453f-136">Esse recurso está disponível a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c453f-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c453f-137">O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</span><span class="sxs-lookup"><span data-stu-id="c453f-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c453f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c453f-138">Requirements</span></span>



| <span data-ttu-id="c453f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c453f-139">Requirement</span></span> | <span data-ttu-id="c453f-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c453f-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c453f-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c453f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c453f-142">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c453f-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c453f-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c453f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c453f-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c453f-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c453f-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c453f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c453f-146"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="c453f-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
