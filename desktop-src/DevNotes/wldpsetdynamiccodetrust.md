---
description: Define um código dinâmico de CRL do .NET em disco confiável para .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Função WldpSetDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370402"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="39bdc-103">Função WldpSetDynamicCodeTrust</span><span class="sxs-lookup"><span data-stu-id="39bdc-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="39bdc-104">Define um código dinâmico de CRL do .NET em disco confiável para .NET.</span><span class="sxs-lookup"><span data-stu-id="39bdc-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bdc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39bdc-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="39bdc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39bdc-107">*FileHandle*</span><span class="sxs-lookup"><span data-stu-id="39bdc-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="39bdc-108">Identificador para um arquivo de código dinâmico em disco.</span><span class="sxs-lookup"><span data-stu-id="39bdc-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39bdc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39bdc-109">Return value</span></span>

<span data-ttu-id="39bdc-110">Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="39bdc-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bdc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39bdc-111">Requirements</span></span>



| <span data-ttu-id="39bdc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bdc-112">Requirement</span></span> | <span data-ttu-id="39bdc-113">Valor</span><span class="sxs-lookup"><span data-stu-id="39bdc-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39bdc-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bdc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="39bdc-115">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="39bdc-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="39bdc-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39bdc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="39bdc-117">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="39bdc-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="39bdc-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39bdc-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bdc-119"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bdc-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="39bdc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="39bdc-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39bdc-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39bdc-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




