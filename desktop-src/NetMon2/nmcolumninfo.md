---
description: A estrutura NMCOLUMNINFO define uma coluna no painel superior da Visualizador de Eventos.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Estrutura NMCOLUMNINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770468"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="51c4a-103">Estrutura NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="51c4a-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="51c4a-104">A estrutura **NMCOLUMNINFO** define uma coluna no painel superior da Visualizador de eventos.</span><span class="sxs-lookup"><span data-stu-id="51c4a-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51c4a-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="51c4a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="51c4a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="51c4a-107">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="51c4a-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="51c4a-108">Nome de exibição de uma coluna específica.</span><span class="sxs-lookup"><span data-stu-id="51c4a-108">Displayable name of a specific column.</span></span> <span data-ttu-id="51c4a-109">Se o nome for muito longo, ele não estará totalmente visível na configuração de Visualizador de Eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="51c4a-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="51c4a-110">**VariantData**</span><span class="sxs-lookup"><span data-stu-id="51c4a-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="51c4a-111">Os dados inseridos na coluna.</span><span class="sxs-lookup"><span data-stu-id="51c4a-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51c4a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51c4a-112">Requirements</span></span>



| <span data-ttu-id="51c4a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c4a-113">Requirement</span></span> | <span data-ttu-id="51c4a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="51c4a-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51c4a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51c4a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51c4a-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51c4a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51c4a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51c4a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51c4a-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51c4a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51c4a-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51c4a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="51c4a-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c4a-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




