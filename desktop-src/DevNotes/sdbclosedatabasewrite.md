---
description: Fecha o banco de dados especificado.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Função SdbCloseDatabaseWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826322"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="957db-103">Função SdbCloseDatabaseWrite</span><span class="sxs-lookup"><span data-stu-id="957db-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="957db-104">Fecha o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="957db-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="957db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="957db-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="957db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="957db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="957db-107">*PDB* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="957db-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="957db-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="957db-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="957db-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="957db-109">Return value</span></span>

<span data-ttu-id="957db-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="957db-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="957db-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="957db-111">Remarks</span></span>

<span data-ttu-id="957db-112">Essa função chama [**SdbCloseDatabase**](sdbclosedatabase.md); Portanto, essas duas funções são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="957db-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="957db-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="957db-113">Requirements</span></span>



| <span data-ttu-id="957db-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="957db-114">Requirement</span></span> | <span data-ttu-id="957db-115">Valor</span><span class="sxs-lookup"><span data-stu-id="957db-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="957db-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="957db-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="957db-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="957db-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="957db-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="957db-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="957db-120">DLL</span><span class="sxs-lookup"><span data-stu-id="957db-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="957db-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="957db-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957db-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="957db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957db-123">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="957db-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="957db-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="957db-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="957db-125">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="957db-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




