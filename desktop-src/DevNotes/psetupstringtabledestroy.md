---
description: Exclui uma tabela de cadeia de caracteres.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: função pSetupStringTableDestroy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753681"
---
# <a name="psetupstringtabledestroy-function"></a><span data-ttu-id="7daf1-103">função pSetupStringTableDestroy</span><span class="sxs-lookup"><span data-stu-id="7daf1-103">pSetupStringTableDestroy function</span></span>

<span data-ttu-id="7daf1-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="7daf1-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="7daf1-105">Exclui uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7daf1-105">Deletes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="7daf1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7daf1-106">Syntax</span></span>


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a><span data-ttu-id="7daf1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7daf1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7daf1-108">*STRINGTABLE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7daf1-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7daf1-109">Um ponteiro para a tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7daf1-109">A pointer to the string table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7daf1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7daf1-110">Return value</span></span>

<span data-ttu-id="7daf1-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7daf1-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7daf1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7daf1-112">Remarks</span></span>

<span data-ttu-id="7daf1-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7daf1-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7daf1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7daf1-114">Requirements</span></span>



| <span data-ttu-id="7daf1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7daf1-115">Requirement</span></span> | <span data-ttu-id="7daf1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7daf1-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7daf1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7daf1-117">DLL</span></span><br/> | <dl> <span data-ttu-id="7daf1-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7daf1-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
