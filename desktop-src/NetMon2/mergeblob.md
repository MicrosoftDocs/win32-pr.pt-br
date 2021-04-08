---
description: A função MergeBlob copia Todas as entradas do BLOB de origem em um BLOB de destino.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Função MergeBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921001"
---
# <a name="mergeblob-function"></a><span data-ttu-id="d1d38-103">Função MergeBlob</span><span class="sxs-lookup"><span data-stu-id="d1d38-103">MergeBlob function</span></span>

<span data-ttu-id="d1d38-104">A função **MergeBlob** copia Todas as entradas do blob de origem em um blob de destino.</span><span class="sxs-lookup"><span data-stu-id="d1d38-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1d38-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d1d38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1d38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d38-107">*hDstBlob* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d1d38-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d38-108">Identificador para o BLOB de destino.</span><span class="sxs-lookup"><span data-stu-id="d1d38-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="d1d38-109">Na entrada, esse BLOB contém suas informações originais.</span><span class="sxs-lookup"><span data-stu-id="d1d38-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="d1d38-110">Na saída, esse BLOB contém suas informações originais e todas as informações do BLOB de origem.</span><span class="sxs-lookup"><span data-stu-id="d1d38-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="d1d38-111">*hSrcBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1d38-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d38-112">Identificador para o BLOB de origem.</span><span class="sxs-lookup"><span data-stu-id="d1d38-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1d38-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1d38-113">Return value</span></span>

<span data-ttu-id="d1d38-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="d1d38-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d1d38-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="d1d38-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d38-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1d38-116">Remarks</span></span>

<span data-ttu-id="d1d38-117">As entradas comuns aos arquivos de origem e de destino serão substituídas pelos dados do BLOB de origem.</span><span class="sxs-lookup"><span data-stu-id="d1d38-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d38-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d38-118">Requirements</span></span>



| <span data-ttu-id="d1d38-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d38-119">Requirement</span></span> | <span data-ttu-id="d1d38-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d1d38-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d38-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d38-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1d38-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d1d38-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1d38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d38-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1d38-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1d38-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1d38-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d38-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d38-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d1d38-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1d38-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1d38-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1d38-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1d38-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d1d38-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d38-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1d38-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




