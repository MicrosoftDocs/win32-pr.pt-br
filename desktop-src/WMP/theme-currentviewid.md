---
title: THEME. currentViewID
description: O atributo currentViewID especifica ou recupera a exibição exibida no momento.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751140"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="1fbf0-104">THEME. currentViewID</span><span class="sxs-lookup"><span data-stu-id="1fbf0-104">THEME.currentViewID</span></span>

<span data-ttu-id="1fbf0-105">O atributo **currentViewID** especifica ou recupera a **exibição** exibida no momento.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="1fbf0-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="1fbf0-106">Possible Values</span></span>

<span data-ttu-id="1fbf0-107">Esse atributo é uma **cadeia de caracteres** de leitura/gravação que especifica a **ID** da **exibição** atual.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="1fbf0-108">Não tem nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fbf0-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fbf0-109">Remarks</span></span>

<span data-ttu-id="1fbf0-110">A especificação de **currentViewID** fecha automaticamente o **modoatual** existente (apontado pelo atributo global **View** ) e abre a **exibição** especificada.</span><span class="sxs-lookup"><span data-stu-id="1fbf0-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="1fbf0-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1fbf0-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="1fbf0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fbf0-112">Requirements</span></span>



| <span data-ttu-id="1fbf0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fbf0-113">Requirement</span></span> | <span data-ttu-id="1fbf0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1fbf0-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="1fbf0-115">Versão</span><span class="sxs-lookup"><span data-stu-id="1fbf0-115">Version</span></span><br/> | <span data-ttu-id="1fbf0-116">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1fbf0-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1fbf0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fbf0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbf0-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="1fbf0-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





