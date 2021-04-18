---
description: Inicializa uma tabela de cadeia de caracteres.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: função pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749172"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="d559c-103">função pSetupStringTableInitializeEx</span><span class="sxs-lookup"><span data-stu-id="d559c-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="d559c-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="d559c-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="d559c-105">Inicializa uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d559c-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d559c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d559c-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="d559c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d559c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d559c-108">*ExtraDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d559c-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d559c-109">Tamanho do objeto de dados extra.</span><span class="sxs-lookup"><span data-stu-id="d559c-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="d559c-110">*Reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="d559c-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d559c-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d559c-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d559c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="d559c-112">Remarks</span></span>

<span data-ttu-id="d559c-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d559c-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d559c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d559c-114">Requirements</span></span>



| <span data-ttu-id="d559c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d559c-115">Requirement</span></span> | <span data-ttu-id="d559c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d559c-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d559c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d559c-117">DLL</span></span><br/> | <dl> <span data-ttu-id="d559c-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d559c-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
