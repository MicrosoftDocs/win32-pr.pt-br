---
description: Determina se os componentes marcados nas opções são instalados no sistema.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: Função IcfgNeedInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755405"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="e4632-103">Função IcfgNeedInetComponents</span><span class="sxs-lookup"><span data-stu-id="e4632-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="e4632-104">Determina se os componentes marcados nas opções são instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="e4632-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4632-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4632-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="e4632-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4632-107">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="e4632-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="e4632-108">Uma combinação dos sinalizadores a seguir que especificam quais componentes detectar da lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4632-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="e4632-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e4632-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="e4632-110">Significado</span><span class="sxs-lookup"><span data-stu-id="e4632-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="e4632-111"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e4632-112">O Exchange ou Internet mail é necessário?</span><span class="sxs-lookup"><span data-stu-id="e4632-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="e4632-113"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="e4632-114">O RAS é necessário?</span><span class="sxs-lookup"><span data-stu-id="e4632-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="e4632-115"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="e4632-116">O TCP/IP é necessário?</span><span class="sxs-lookup"><span data-stu-id="e4632-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="e4632-117">*lpfNeedComponents*</span><span class="sxs-lookup"><span data-stu-id="e4632-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="e4632-118">Se esse valor for não **nulo**, ele será **verdadeiro** no retorno se um ou mais componentes não estiverem instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="e4632-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4632-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4632-119">Return value</span></span>

<span data-ttu-id="e4632-120">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4632-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4632-121">Se nenhum erro ocorrer, ele retornará o código de **\_ êxito do erro** .</span><span class="sxs-lookup"><span data-stu-id="e4632-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4632-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4632-122">Remarks</span></span>

<span data-ttu-id="e4632-123">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e4632-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4632-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4632-124">Requirements</span></span>



| <span data-ttu-id="e4632-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4632-125">Requirement</span></span> | <span data-ttu-id="e4632-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e4632-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4632-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e4632-127">DLL</span></span><br/> | <dl> <span data-ttu-id="e4632-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4632-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
