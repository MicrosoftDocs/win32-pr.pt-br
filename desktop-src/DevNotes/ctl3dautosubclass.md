---
description: Subclasses automaticamente e adiciona efeitos 3D a todas as caixas de diálogo no aplicativo.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Função Ctl3dAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748498"
---
# <a name="ctl3dautosubclass-function"></a><span data-ttu-id="21e23-103">Função Ctl3dAutoSubclass</span><span class="sxs-lookup"><span data-stu-id="21e23-103">Ctl3dAutoSubclass function</span></span>

<span data-ttu-id="21e23-104">Subclasses automaticamente e adiciona efeitos 3D a todas as caixas de diálogo no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21e23-104">Automatically subclasses and adds 3D effects to all dialog boxes in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e23-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21e23-105">Syntax</span></span>


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="21e23-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21e23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e23-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="21e23-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="21e23-108">Um identificador para o aplicativo a ser registrado como um cliente.</span><span class="sxs-lookup"><span data-stu-id="21e23-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e23-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21e23-109">Return value</span></span>

<span data-ttu-id="21e23-110">Retorna **true** , a menos que uma das condições a seguir exista, caso em que ela retorna **false**:</span><span class="sxs-lookup"><span data-stu-id="21e23-110">Returns **TRUE** unless one of the following conditions exists, in which case it returns **FALSE**:</span></span>

-   <span data-ttu-id="21e23-111">O CTL3D está em execução no Windows versão 3,0 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="21e23-111">CTL3D is running under Windows version 3.0 or earlier.</span></span>
-   <span data-ttu-id="21e23-112">CTL3D não tem espaço disponível em suas tabelas para o aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="21e23-112">CTL3D does not have space available in its tables for the current application.</span></span> <span data-ttu-id="21e23-113">O CTL3D pode atender até 32 aplicativos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="21e23-113">CTL3D can service up to 32 applications at the same time.</span></span>
-   <span data-ttu-id="21e23-114">CTL3D não pode instalar seu gancho de CBT.</span><span class="sxs-lookup"><span data-stu-id="21e23-114">CTL3D cannot install its CBT hook.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e23-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="21e23-115">Remarks</span></span>

<span data-ttu-id="21e23-116">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="21e23-116">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e23-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21e23-117">Requirements</span></span>



| <span data-ttu-id="21e23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="21e23-118">Requirement</span></span> | <span data-ttu-id="21e23-119">Valor</span><span class="sxs-lookup"><span data-stu-id="21e23-119">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21e23-120">DLL</span><span class="sxs-lookup"><span data-stu-id="21e23-120">DLL</span></span><br/> | <dl> <span data-ttu-id="21e23-121"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e23-121"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
