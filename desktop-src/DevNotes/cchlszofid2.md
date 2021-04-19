---
description: Decodifica e armazena uma cadeia de caracteres.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Função CchLszOfId2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747628"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="2a29b-103">Função CchLszOfId2</span><span class="sxs-lookup"><span data-stu-id="2a29b-103">CchLszOfId2 function</span></span>

<span data-ttu-id="2a29b-104">Decodifica e armazena uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2a29b-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a29b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a29b-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="2a29b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a29b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a29b-107">*id*</span><span class="sxs-lookup"><span data-stu-id="2a29b-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="2a29b-108">O identificador da cadeia de caracteres no arquivo de recurso a ser decodificado e armazenado.</span><span class="sxs-lookup"><span data-stu-id="2a29b-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="2a29b-109">A validade da cadeia de caracteres não é verificada.</span><span class="sxs-lookup"><span data-stu-id="2a29b-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="2a29b-110">*lsz*</span><span class="sxs-lookup"><span data-stu-id="2a29b-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="2a29b-111">Um ponteiro para um buffer com um comprimento de *cbMax*.</span><span class="sxs-lookup"><span data-stu-id="2a29b-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="2a29b-112">Cadeias de caracteres maiores que *cbMax* são truncadas.</span><span class="sxs-lookup"><span data-stu-id="2a29b-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="2a29b-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="2a29b-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="2a29b-114">O comprimento máximo da cadeia de caracteres a ser armazenada no parâmetro *LSZ* .</span><span class="sxs-lookup"><span data-stu-id="2a29b-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a29b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a29b-115">Return value</span></span>

<span data-ttu-id="2a29b-116">Essa função retorna a cadeia de caracteres decodificada.</span><span class="sxs-lookup"><span data-stu-id="2a29b-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a29b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a29b-117">Remarks</span></span>

<span data-ttu-id="2a29b-118">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2a29b-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a29b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a29b-119">Requirements</span></span>



| <span data-ttu-id="2a29b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a29b-120">Requirement</span></span> | <span data-ttu-id="2a29b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2a29b-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a29b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2a29b-122">DLL</span></span><br/> | <dl> <span data-ttu-id="2a29b-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a29b-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
