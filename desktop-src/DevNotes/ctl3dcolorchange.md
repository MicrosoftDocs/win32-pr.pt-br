---
description: Manipula alterações de cores do sistema para aplicativos que usam CTL3D.
ms.assetid: b1eadb7d-39a5-47e9-9ae5-62bd33557f6b
title: Função Ctl3dColorChange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dColorChange
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 7e7b0d4480fde480ea24a6c2c0dd8a7a849fbc75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750287"
---
# <a name="ctl3dcolorchange-function"></a><span data-ttu-id="432b0-103">Função Ctl3dColorChange</span><span class="sxs-lookup"><span data-stu-id="432b0-103">Ctl3dColorChange function</span></span>

<span data-ttu-id="432b0-104">Manipula alterações de cores do sistema para aplicativos que usam CTL3D.</span><span class="sxs-lookup"><span data-stu-id="432b0-104">Handles system color changes for applications that use CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="432b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="432b0-105">Syntax</span></span>


```C++
BOOL Ctl3dColorChange(void);
```



## <a name="parameters"></a><span data-ttu-id="432b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="432b0-106">Parameters</span></span>

<span data-ttu-id="432b0-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="432b0-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="432b0-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="432b0-108">Return value</span></span>

<span data-ttu-id="432b0-109">Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="432b0-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="432b0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="432b0-110">Remarks</span></span>

<span data-ttu-id="432b0-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="432b0-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="432b0-112">Essa função deve ser chamada no procedimento da janela principal do aplicativo para a **mensagem \_ SYSCOLORCHANGE do WM** , como mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="432b0-112">This function should be called in the application's main window procedure for the **WM\_SYSCOLORCHANGE** message, as shown below.</span></span>

## <a name="examples"></a><span data-ttu-id="432b0-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="432b0-113">Examples</span></span>

``` syntax
case WM_SYSCOLORCHANGE:
   Ctl3dColorChange();
   break;
```

## <a name="requirements"></a><span data-ttu-id="432b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="432b0-114">Requirements</span></span>



| <span data-ttu-id="432b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="432b0-115">Requirement</span></span> | <span data-ttu-id="432b0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="432b0-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="432b0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="432b0-117">DLL</span></span><br/> | <dl> <span data-ttu-id="432b0-118"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="432b0-118"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
