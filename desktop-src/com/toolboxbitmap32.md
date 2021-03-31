---
title: ToolBoxBitmap32
description: Identifica o nome do módulo e a ID de recurso para um bitmap de 16 x 16 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.
ms.assetid: 87b3d8e1-4d54-465c-9e5e-5e4f7391f313
keywords:
- ToolBoxBitmap32 de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ca6208586e961c0b6f8fa666c5731bab38faa6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005340"
---
# <a name="toolboxbitmap32"></a><span data-ttu-id="093b6-104">ToolBoxBitmap32</span><span class="sxs-lookup"><span data-stu-id="093b6-104">ToolBoxBitmap32</span></span>

<span data-ttu-id="093b6-105">Identifica o nome do módulo e a ID de recurso para um bitmap de 16 x 16 a ser usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="093b6-105">Identifies the module name and resource ID for a 16 x 16 bitmap to use for the face of a toolbar or toolbox button.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="093b6-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="093b6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ToolBoxBitmap32 = filename,  resourceID
```

## <a name="remarks"></a><span data-ttu-id="093b6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="093b6-107">Remarks</span></span>

<span data-ttu-id="093b6-108">Este é um valor de **\_ sz de reg** que especifica o nome do módulo e o identificador de recurso para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="093b6-108">This is a **REG\_SZ** value that specifies the module name and resource identifier for the bitmap.</span></span>

<span data-ttu-id="093b6-109">O tamanho do ícone padrão do Windows é muito grande para ser usado para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="093b6-109">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="093b6-110">Isso requer contêineres de controle que têm um modo de design no qual um seleciona os controles e os coloca em um formulário que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="093b6-110">This requires control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span>

 

 




