---
description: A função RegOpenBlobKey recupera um BLOB armazenado na chave do registro fornecida.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Função RegOpenBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812888"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="a0a6f-103">Função RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="a0a6f-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="a0a6f-104">A função **RegOpenBlobKey** recupera um blob armazenado na chave do registro fornecida.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a6f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0a6f-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="a0a6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a6f-107">*HKEY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0a6f-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6f-108">Identificador para a chave do registro que contém o BLOB.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="a0a6f-109">*szBlobName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0a6f-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6f-110">Nome que identifica o BLOB especificado no registro.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="a0a6f-111">*phBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a0a6f-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0a6f-112">Ponteiro para o BLOB que é recuperado.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a6f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0a6f-113">Return value</span></span>

<span data-ttu-id="a0a6f-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a0a6f-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="a0a6f-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0a6f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a6f-116">Requirements</span></span>



| <span data-ttu-id="a0a6f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a6f-117">Requirement</span></span> | <span data-ttu-id="a0a6f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a0a6f-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a6f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a6f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a6f-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a6f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a0a6f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0a6f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a6f-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0a6f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0a6f-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0a6f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0a6f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a6f-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a0a6f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0a6f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a0a6f-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0a6f-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a0a6f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a6f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a6f-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a6f-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a6f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0a6f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a6f-130">RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="a0a6f-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




