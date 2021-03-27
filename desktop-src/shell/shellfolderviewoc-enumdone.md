---
description: Indica que o objeto ShellFolderView terminou de enumerar o conteúdo da pasta.
title: Evento ShellFolderViewOC. EnumDone (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989060"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="fd0ec-103">Evento ShellFolderViewOC. EnumDone</span><span class="sxs-lookup"><span data-stu-id="fd0ec-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="fd0ec-104">Indica que o objeto [**ShellFolderView**](shellfolderview.md) terminou de enumerar o conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd0ec-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="fd0ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd0ec-106">Parameters</span></span>

<span data-ttu-id="fd0ec-107">Este manipulador de eventos não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0ec-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd0ec-108">Remarks</span></span>

<span data-ttu-id="fd0ec-109">O objeto [**ShellFolderView**](shellfolderview.md) deve enumerar o conteúdo de uma pasta para poder exibi-la.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="fd0ec-110">Com pastas grandes ou localizadas em um sistema remoto, esse processo pode levar até vários minutos.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="fd0ec-111">Durante esse tempo, um gráfico de lanterna animada é exibido para indicar ao usuário que o processamento está sob o caminho.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="fd0ec-112">Depois que a enumeração for concluída, o evento **EnumDone** será acionado e o gráfico de lanterna será substituído pelo conteúdo da pasta.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="fd0ec-113">Forneça o código de manipulação de eventos para esse evento, conforme mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="fd0ec-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="fd0ec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd0ec-114">Requirements</span></span>



| <span data-ttu-id="fd0ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd0ec-115">Requirement</span></span> | <span data-ttu-id="fd0ec-116">Valor</span><span class="sxs-lookup"><span data-stu-id="fd0ec-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0ec-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd0ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0ec-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fd0ec-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd0ec-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd0ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0ec-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd0ec-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd0ec-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd0ec-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0ec-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ec-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fd0ec-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="fd0ec-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd0ec-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ec-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fd0ec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fd0ec-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd0ec-126"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fd0ec-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0ec-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd0ec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0ec-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="fd0ec-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




