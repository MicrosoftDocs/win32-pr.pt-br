---
title: MiscStatus
description: Especifica como criar e exibir um objeto.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005746"
---
# <a name="miscstatus"></a><span data-ttu-id="0c100-104">MiscStatus</span><span class="sxs-lookup"><span data-stu-id="0c100-104">MiscStatus</span></span>

<span data-ttu-id="0c100-105">Especifica como criar e exibir um objeto.</span><span class="sxs-lookup"><span data-stu-id="0c100-105">Specifies how to create and display an object.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0c100-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="0c100-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a><span data-ttu-id="0c100-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c100-107">Remarks</span></span>

<span data-ttu-id="0c100-108">Para obter mais informações, consulte a enumeração [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) e [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span><span class="sxs-lookup"><span data-stu-id="0c100-108">For more information, see the [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) enumeration and [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).</span></span>

<span data-ttu-id="0c100-109">Se nenhuma subchave correspondente a um DVASPECT for encontrada, o valor padrão de **MiscStatus** será usado.</span><span class="sxs-lookup"><span data-stu-id="0c100-109">If no subkey that corresponds to a DVASPECT is found, the default value of **MiscStatus** is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c100-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c100-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c100-111">**IOleObject::GetMiscStatus**</span><span class="sxs-lookup"><span data-stu-id="0c100-111">**IOleObject::GetMiscStatus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




