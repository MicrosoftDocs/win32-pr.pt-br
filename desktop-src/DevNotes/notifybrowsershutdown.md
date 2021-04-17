---
description: Libera carregadores de classe Java que podem ter sido consumidos ao navegar pelos applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Função NotifyBrowserShutdown
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754909"
---
# <a name="notifybrowsershutdown-function"></a><span data-ttu-id="77a30-103">Função NotifyBrowserShutdown</span><span class="sxs-lookup"><span data-stu-id="77a30-103">NotifyBrowserShutdown function</span></span>

<span data-ttu-id="77a30-104">Libera carregadores de classe Java que podem ter sido consumidos ao navegar pelos applets.</span><span class="sxs-lookup"><span data-stu-id="77a30-104">Frees Java class loaders that may have been consumed while browsing the applets.</span></span>

## <a name="syntax"></a><span data-ttu-id="77a30-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77a30-105">Syntax</span></span>


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="77a30-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77a30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a30-107">*lpvReserved*</span><span class="sxs-lookup"><span data-stu-id="77a30-107">*lpvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="77a30-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="77a30-108">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a30-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77a30-109">Return value</span></span>

<span data-ttu-id="77a30-110">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="77a30-110">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="77a30-111">Caso contrário, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="77a30-111">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="77a30-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="77a30-112">Remarks</span></span>

<span data-ttu-id="77a30-113">Quando a contagem de janelas do navegador atinge zero no modo Web integrado, essa função libera os carregadores de classe Java.</span><span class="sxs-lookup"><span data-stu-id="77a30-113">When the count of browser windows reaches zero in integrated Web mode, this function frees the Java class loaders.</span></span> <span data-ttu-id="77a30-114">Quando o usuário começa a procurar novamente os applets, a VM Java baixará os arquivos de classe mais recentes.</span><span class="sxs-lookup"><span data-stu-id="77a30-114">When the user starts browsing applets again, the Java VM will download the latest class files.</span></span>

<span data-ttu-id="77a30-115">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="77a30-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="77a30-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77a30-116">Requirements</span></span>



| <span data-ttu-id="77a30-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77a30-117">Requirement</span></span> | <span data-ttu-id="77a30-118">Valor</span><span class="sxs-lookup"><span data-stu-id="77a30-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77a30-119">DLL</span><span class="sxs-lookup"><span data-stu-id="77a30-119">DLL</span></span><br/> | <dl> <span data-ttu-id="77a30-120"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77a30-120"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
