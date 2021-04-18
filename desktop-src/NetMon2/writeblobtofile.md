---
description: A função WriteBlobToFile grava um BLOB em um arquivo.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Função WriteBlobToFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755579"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="c138d-103">Função WriteBlobToFile</span><span class="sxs-lookup"><span data-stu-id="c138d-103">WriteBlobToFile function</span></span>

<span data-ttu-id="c138d-104">A função **WriteBlobToFile** grava um blob em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c138d-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c138d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c138d-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c138d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c138d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c138d-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c138d-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c138d-108">Identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="c138d-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c138d-109">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c138d-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c138d-110">Ponteiro para o nome do arquivo, no qual o BLOB é salvo.</span><span class="sxs-lookup"><span data-stu-id="c138d-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c138d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c138d-111">Return value</span></span>

<span data-ttu-id="c138d-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c138d-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c138d-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="c138d-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c138d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c138d-114">Requirements</span></span>



| <span data-ttu-id="c138d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c138d-115">Requirement</span></span> | <span data-ttu-id="c138d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c138d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c138d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c138d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c138d-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c138d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c138d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c138d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c138d-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c138d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c138d-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c138d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c138d-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c138d-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c138d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c138d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c138d-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c138d-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c138d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c138d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c138d-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c138d-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




