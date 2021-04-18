---
description: Instala os componentes do sistema especificados.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: Função IcfgInstallInetComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749713"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="d3c2f-103">Função IcfgInstallInetComponents</span><span class="sxs-lookup"><span data-stu-id="d3c2f-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="d3c2f-104">Instala os componentes do sistema especificados.</span><span class="sxs-lookup"><span data-stu-id="d3c2f-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3c2f-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="d3c2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3c2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c2f-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="d3c2f-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c2f-108">Um identificador para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="d3c2f-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="d3c2f-109">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="d3c2f-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c2f-110">Uma combinação dos sinalizadores a seguir que controlam a instalação e a configuração.</span><span class="sxs-lookup"><span data-stu-id="d3c2f-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="d3c2f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c2f-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="d3c2f-112">Significado</span><span class="sxs-lookup"><span data-stu-id="d3c2f-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="d3c2f-113"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d3c2f-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="d3c2f-114">Instale o Exchange e o Internet mail.</span><span class="sxs-lookup"><span data-stu-id="d3c2f-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="d3c2f-115"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d3c2f-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="d3c2f-116">Instale o RAS (se necessário).</span><span class="sxs-lookup"><span data-stu-id="d3c2f-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="d3c2f-117"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d3c2f-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="d3c2f-118">Instale o TCP/IP (se necessário).</span><span class="sxs-lookup"><span data-stu-id="d3c2f-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="d3c2f-119">*lpfNeedsRestart*</span><span class="sxs-lookup"><span data-stu-id="d3c2f-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="d3c2f-120">Se esse valor for não **nulo**, em retorno será **verdadeiro** somente se o Windows precisar ser reiniciado para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="d3c2f-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c2f-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3c2f-121">Return value</span></span>

<span data-ttu-id="d3c2f-122">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3c2f-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d3c2f-123">Se nenhum erro ocorrer, ele retornará o código de **\_ êxito do erro** .</span><span class="sxs-lookup"><span data-stu-id="d3c2f-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c2f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3c2f-124">Remarks</span></span>

<span data-ttu-id="d3c2f-125">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d3c2f-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c2f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3c2f-126">Requirements</span></span>



| <span data-ttu-id="d3c2f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c2f-127">Requirement</span></span> | <span data-ttu-id="d3c2f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d3c2f-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c2f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c2f-129">DLL</span></span><br/> | <dl> <span data-ttu-id="d3c2f-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c2f-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
