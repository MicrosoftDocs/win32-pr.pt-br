---
description: O método CloseDatabase do objeto de mesclagem fecha o banco de dados Windows Installer aberto no momento.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Método Merge. CloseDatabase (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757793"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="41bc2-103">Método Merge. CloseDatabase</span><span class="sxs-lookup"><span data-stu-id="41bc2-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="41bc2-104">O método **CloseDatabase** do objeto de [**mesclagem**](merge-object.md) fecha o banco de dados Windows Installer aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="41bc2-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="41bc2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41bc2-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="41bc2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41bc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41bc2-107">*bCommit*</span><span class="sxs-lookup"><span data-stu-id="41bc2-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="41bc2-108">**True** se as alterações devem ser salvas; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="41bc2-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41bc2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41bc2-109">Return value</span></span>

<span data-ttu-id="41bc2-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="41bc2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41bc2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="41bc2-111">Remarks</span></span>

<span data-ttu-id="41bc2-112">Fechar um banco de dados limpa todas as informações de dependência, mas não afeta os erros que não foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="41bc2-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="41bc2-113">C++</span><span class="sxs-lookup"><span data-stu-id="41bc2-113">C++</span></span>

<span data-ttu-id="41bc2-114">Consulte a função [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="41bc2-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41bc2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41bc2-115">Requirements</span></span>



| <span data-ttu-id="41bc2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41bc2-116">Requirement</span></span> | <span data-ttu-id="41bc2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="41bc2-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41bc2-118">Versão</span><span class="sxs-lookup"><span data-stu-id="41bc2-118">Version</span></span><br/> | <span data-ttu-id="41bc2-119">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="41bc2-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="41bc2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41bc2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="41bc2-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="41bc2-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="41bc2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="41bc2-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="41bc2-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41bc2-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
