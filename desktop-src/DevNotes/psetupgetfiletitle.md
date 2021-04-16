---
description: Recupera o título do arquivo para o caminho de arquivo especificado.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: função pSetupGetFileTitle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751551"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="3f995-103">função pSetupGetFileTitle</span><span class="sxs-lookup"><span data-stu-id="3f995-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="3f995-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="3f995-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="3f995-105">Recupera o título do arquivo para o caminho de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3f995-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f995-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f995-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="3f995-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f995-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f995-108">*FilePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f995-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f995-109">O caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3f995-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f995-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f995-110">Return value</span></span>

<span data-ttu-id="3f995-111">Um ponteiro para cadeia de caracteres que recebe o título do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3f995-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f995-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f995-112">Remarks</span></span>

<span data-ttu-id="3f995-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3f995-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f995-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f995-114">Requirements</span></span>



| <span data-ttu-id="3f995-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f995-115">Requirement</span></span> | <span data-ttu-id="3f995-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3f995-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f995-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3f995-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3f995-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f995-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
