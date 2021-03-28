---
description: Define os pontos dos objetos atualmente selecionados para o objeto de dados nos comandos copiar e recortar. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETPOINTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172071"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="29651-104">Mensagem de SFVM \_ SETpoints</span><span class="sxs-lookup"><span data-stu-id="29651-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="29651-105">Define os pontos dos objetos atualmente selecionados para o objeto de dados nos comandos **copiar** e **recortar** .</span><span class="sxs-lookup"><span data-stu-id="29651-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="29651-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="29651-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="29651-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29651-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29651-108">*pdtobj* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29651-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="29651-109">Um ponteiro para um <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> dos comandos **copiar** e **recortar** .</span><span class="sxs-lookup"><span data-stu-id="29651-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29651-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29651-110">Return value</span></span>

<span data-ttu-id="29651-111">Sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="29651-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="29651-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="29651-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="29651-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29651-113">Requirements</span></span>



| <span data-ttu-id="29651-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="29651-114">Requirement</span></span> | <span data-ttu-id="29651-115">Valor</span><span class="sxs-lookup"><span data-stu-id="29651-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29651-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29651-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29651-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="29651-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="29651-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29651-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29651-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="29651-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="29651-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="29651-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="29651-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="29651-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
