---
description: A função RegCreateBlobKey armazena um BLOB na chave do registro fornecida.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Função RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768586"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="eaa82-103">Função RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="eaa82-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="eaa82-104">A função **RegCreateBlobKey** armazena um blob na chave do registro fornecida.</span><span class="sxs-lookup"><span data-stu-id="eaa82-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eaa82-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="eaa82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eaa82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa82-107">*HKEY* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="eaa82-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa82-108">Manipule a chave do registro onde o BLOB será armazenado.</span><span class="sxs-lookup"><span data-stu-id="eaa82-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="eaa82-109">*szBlobName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eaa82-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa82-110">Nome (definido pelo aplicativo) que representa o BLOB no registro.</span><span class="sxs-lookup"><span data-stu-id="eaa82-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="eaa82-111">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eaa82-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaa82-112">Identificador para o BLOB que é salvo.</span><span class="sxs-lookup"><span data-stu-id="eaa82-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa82-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eaa82-113">Return value</span></span>

<span data-ttu-id="eaa82-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="eaa82-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="eaa82-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="eaa82-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa82-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaa82-116">Requirements</span></span>



| <span data-ttu-id="eaa82-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaa82-117">Requirement</span></span> | <span data-ttu-id="eaa82-118">Valor</span><span class="sxs-lookup"><span data-stu-id="eaa82-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa82-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaa82-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa82-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eaa82-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eaa82-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eaa82-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa82-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="eaa82-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaa82-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="eaa82-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa82-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa82-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="eaa82-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eaa82-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="eaa82-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eaa82-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="eaa82-127">DLL</span><span class="sxs-lookup"><span data-stu-id="eaa82-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaa82-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaa82-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaa82-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaa82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa82-130">RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="eaa82-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




