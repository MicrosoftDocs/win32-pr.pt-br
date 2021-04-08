---
description: Define uma opção de entrada Microsoft .NET Passport específica.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: 'IPassportManager3: método de ut_Option de:p'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920157"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="85d3c-103">Método de opção IPassportManager3::p UT \_</span><span class="sxs-lookup"><span data-stu-id="85d3c-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="85d3c-104">Define uma opção de entrada Microsoft .NET Passport específica.</span><span class="sxs-lookup"><span data-stu-id="85d3c-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="85d3c-105">O método de **\_ opção Put** pertence à interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="85d3c-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="85d3c-106">Este tópico complementa a documentação inicial.</span><span class="sxs-lookup"><span data-stu-id="85d3c-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="85d3c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85d3c-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="85d3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85d3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d3c-109">*name*</span><span class="sxs-lookup"><span data-stu-id="85d3c-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="85d3c-110">A opção de entrada a ser definida.</span><span class="sxs-lookup"><span data-stu-id="85d3c-110">The sign-in option to be set.</span></span> <span data-ttu-id="85d3c-111">Atualmente, a única opção com suporte é iMode.</span><span class="sxs-lookup"><span data-stu-id="85d3c-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="85d3c-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="85d3c-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="85d3c-113">Uma **variante** (VT \_ bool) que especifica o novo valor para a opção.</span><span class="sxs-lookup"><span data-stu-id="85d3c-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="85d3c-114">Esse valor pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="85d3c-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d3c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85d3c-115">Return value</span></span>

<span data-ttu-id="85d3c-116">Retorna S \_ OK quando o método for bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="85d3c-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d3c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="85d3c-117">Remarks</span></span>

<span data-ttu-id="85d3c-118">Esse método é fornecido com versões mais antigas do SDK do Passport.</span><span class="sxs-lookup"><span data-stu-id="85d3c-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
