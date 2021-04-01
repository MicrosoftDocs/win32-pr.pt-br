---
description: A função IsRemoteNPP indica se o BLOB especificado especifica um NPP remoto.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Função IsRemoteNPP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661854"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="3a08f-103">Função IsRemoteNPP</span><span class="sxs-lookup"><span data-stu-id="3a08f-103">IsRemoteNPP function</span></span>

<span data-ttu-id="3a08f-104">A função **IsRemoteNPP** indica se o blob especificado especifica um NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="3a08f-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a08f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a08f-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3a08f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a08f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a08f-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3a08f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a08f-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="3a08f-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a08f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a08f-109">Return value</span></span>

<span data-ttu-id="3a08f-110">Se a função for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="3a08f-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a08f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a08f-111">Remarks</span></span>

<span data-ttu-id="3a08f-112">Use essa função para testar se existe uma categoria remota.</span><span class="sxs-lookup"><span data-stu-id="3a08f-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="3a08f-113">Verifique se os nomes dos computadores remotos e locais são diferentes.</span><span class="sxs-lookup"><span data-stu-id="3a08f-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a08f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a08f-114">Requirements</span></span>



| <span data-ttu-id="3a08f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a08f-115">Requirement</span></span> | <span data-ttu-id="3a08f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3a08f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a08f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a08f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3a08f-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a08f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3a08f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a08f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3a08f-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a08f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3a08f-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a08f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a08f-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a08f-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3a08f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a08f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a08f-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a08f-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3a08f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3a08f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a08f-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a08f-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




