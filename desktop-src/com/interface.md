---
title: Interface (COM)
description: Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chave do registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105793346"
---
# <a name="interface-com"></a><span data-ttu-id="931d5-104">Interface (COM)</span><span class="sxs-lookup"><span data-stu-id="931d5-104">Interface (COM)</span></span>

<span data-ttu-id="931d5-105">Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.</span><span class="sxs-lookup"><span data-stu-id="931d5-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="931d5-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="931d5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="931d5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="931d5-107">Remarks</span></span>

<span data-ttu-id="931d5-108">Se um nome de interface não estiver presente nessa lista, a interface nunca poderá ser suportada por uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="931d5-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="931d5-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="931d5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="931d5-110">Chave de Interface</span><span class="sxs-lookup"><span data-stu-id="931d5-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




