---
description: A função ReadBlobFromFile lê um BLOB em um arquivo.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Função ReadBlobFromFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759481"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="bdf94-103">Função ReadBlobFromFile</span><span class="sxs-lookup"><span data-stu-id="bdf94-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="bdf94-104">A função **ReadBlobFromFile** lê um blob em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="bdf94-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf94-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdf94-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="bdf94-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf94-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdf94-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf94-108">Identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="bdf94-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="bdf94-109">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bdf94-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdf94-110">Ponteiro para o nome do arquivo que contém o BLOB.</span><span class="sxs-lookup"><span data-stu-id="bdf94-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf94-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bdf94-111">Return value</span></span>

<span data-ttu-id="bdf94-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="bdf94-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bdf94-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="bdf94-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf94-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf94-114">Requirements</span></span>



| <span data-ttu-id="bdf94-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf94-115">Requirement</span></span> | <span data-ttu-id="bdf94-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf94-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf94-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf94-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf94-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf94-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bdf94-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf94-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf94-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf94-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bdf94-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bdf94-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf94-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf94-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bdf94-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdf94-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdf94-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdf94-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdf94-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bdf94-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdf94-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdf94-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




