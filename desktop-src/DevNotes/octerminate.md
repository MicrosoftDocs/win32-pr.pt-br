---
description: Fecha o Gerenciador de OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Função OcTerminate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752767"
---
# <a name="octerminate-function"></a><span data-ttu-id="f36a6-103">Função OcTerminate</span><span class="sxs-lookup"><span data-stu-id="f36a6-103">OcTerminate function</span></span>

<span data-ttu-id="f36a6-104">Fecha o Gerenciador de OC.</span><span class="sxs-lookup"><span data-stu-id="f36a6-104">Closes the OC manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f36a6-105">Syntax</span></span>


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a><span data-ttu-id="f36a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f36a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f36a6-107">*OcManagerContext* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f36a6-107">*OcManagerContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f36a6-108">Na entrada, contém o ponteiro de contexto do Gerenciador OC retornado por [**OcInitialize**](ocinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="f36a6-108">On input, contains the OC manager context pointer returned by [**OcInitialize**](ocinitialize.md).</span></span> <span data-ttu-id="f36a6-109">Na saída, recebe **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f36a6-109">On output, receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f36a6-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f36a6-110">Return value</span></span>

<span data-ttu-id="f36a6-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f36a6-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f36a6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f36a6-112">Remarks</span></span>

<span data-ttu-id="f36a6-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f36a6-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36a6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f36a6-114">Requirements</span></span>



| <span data-ttu-id="f36a6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f36a6-115">Requirement</span></span> | <span data-ttu-id="f36a6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f36a6-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36a6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f36a6-117">DLL</span></span><br/> | <dl> <span data-ttu-id="f36a6-118"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f36a6-118"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f36a6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f36a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36a6-120">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="f36a6-120">**OcInitialize**</span></span>](ocinitialize.md)
</dt> </dl>

 

 
