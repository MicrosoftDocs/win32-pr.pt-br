---
description: Cria ou abre um arquivo.
ms.assetid: 2a993f45-7f87-4b9e-bccc-277477558d3c
title: Função _CreateFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _CreateFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: becd7fed9e32385409b78e00169191a12b550e3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749062"
---
# <a name="_createfile-function"></a><span data-ttu-id="8fcdf-103">\_Função CreateFile</span><span class="sxs-lookup"><span data-stu-id="8fcdf-103">\_CreateFile function</span></span>

<span data-ttu-id="8fcdf-104">\[Essa função é um wrapper sobre a função **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="8fcdf-104">\[This function is a wrapper over the **CreateFile** function.</span></span> <span data-ttu-id="8fcdf-105">Essa função pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="8fcdf-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="8fcdf-106">Os aplicativos devem chamar **CreateFile** diretamente.\]</span><span class="sxs-lookup"><span data-stu-id="8fcdf-106">Applications should call **CreateFile** directly.\]</span></span>

<span data-ttu-id="8fcdf-107">Cria ou abre um arquivo.</span><span class="sxs-lookup"><span data-stu-id="8fcdf-107">Creates or opens a file.</span></span> <span data-ttu-id="8fcdf-108">Consulte [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="8fcdf-108">See [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcdf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fcdf-109">Syntax</span></span>


```C++
BOOL _CreateFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="8fcdf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fcdf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fcdf-111">*...*</span><span class="sxs-lookup"><span data-stu-id="8fcdf-111">*...*</span></span> 
<span data-ttu-id="8fcdf-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8fcdf-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8fcdf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fcdf-113">Requirements</span></span>



| <span data-ttu-id="8fcdf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fcdf-114">Requirement</span></span> | <span data-ttu-id="8fcdf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8fcdf-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcdf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8fcdf-116">DLL</span></span><br/> | <dl> <span data-ttu-id="8fcdf-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fcdf-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcdf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fcdf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcdf-119">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="8fcdf-119">**CreateFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> </dl>

 

