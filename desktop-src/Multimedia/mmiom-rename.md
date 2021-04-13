---
title: Mensagem de MMIOM_RENAME (mmsystem. h)
description: A \_ mensagem de renomeação MMIOM é enviada a um procedimento de e/s pela função mmioRename para solicitar que o arquivo especificado seja renomeado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- Multimídia do Windows de mensagem MMIOM_RENAME
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455726"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="a98ce-104">MMIOM \_ renomear mensagem</span><span class="sxs-lookup"><span data-stu-id="a98ce-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="a98ce-105">A mensagem de **\_ renomeação MMIOM** é enviada a um procedimento de e/s pela função [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) para solicitar que o arquivo especificado seja renomeado.</span><span class="sxs-lookup"><span data-stu-id="a98ce-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="a98ce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a98ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a98ce-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span><span class="sxs-lookup"><span data-stu-id="a98ce-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="a98ce-108">Ponteiro para uma cadeia de caracteres que contém o nome do arquivo a ser renomeado.</span><span class="sxs-lookup"><span data-stu-id="a98ce-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="a98ce-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span><span class="sxs-lookup"><span data-stu-id="a98ce-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="a98ce-110">Ponteiro para uma cadeia de caracteres que contém o novo nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a98ce-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a98ce-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a98ce-111">Return Value</span></span>

<span data-ttu-id="a98ce-112">Se o arquivo for renomeado com êxito, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="a98ce-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="a98ce-113">Se o arquivo especificado não foi encontrado, o valor de retorno será MMIOERR \_ FILENOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="a98ce-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98ce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a98ce-114">Requirements</span></span>



| <span data-ttu-id="a98ce-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a98ce-115">Requirement</span></span> | <span data-ttu-id="a98ce-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a98ce-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98ce-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a98ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a98ce-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a98ce-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a98ce-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a98ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a98ce-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a98ce-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a98ce-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a98ce-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a98ce-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a98ce-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

