---
description: Recarrega uma configuração do IME do Registro HKCU, somente no IME do japonês.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: função reload_config
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755753"
---
# <a name="reload_config-function"></a><span data-ttu-id="75da8-103">recarregar \_ função de configuração</span><span class="sxs-lookup"><span data-stu-id="75da8-103">reload\_config function</span></span>

<span data-ttu-id="75da8-104">Recarrega uma configuração do IME do Registro HKCU, somente no IME do japonês.</span><span class="sxs-lookup"><span data-stu-id="75da8-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75da8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75da8-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="75da8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75da8-106">Parameters</span></span>

<span data-ttu-id="75da8-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="75da8-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75da8-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="75da8-108">Return value</span></span>

<span data-ttu-id="75da8-109">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="75da8-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="75da8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="75da8-110">Remarks</span></span>

<span data-ttu-id="75da8-111">Se nenhum valor de registro estiver presente em HKCU, a função **recarregar \_ config** gravará os dados iniciais no registro.</span><span class="sxs-lookup"><span data-stu-id="75da8-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="75da8-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="75da8-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="75da8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75da8-113">Requirements</span></span>



| <span data-ttu-id="75da8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="75da8-114">Requirement</span></span> | <span data-ttu-id="75da8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="75da8-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75da8-116">DLL</span><span class="sxs-lookup"><span data-stu-id="75da8-116">DLL</span></span><br/> | <dl> <span data-ttu-id="75da8-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75da8-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
