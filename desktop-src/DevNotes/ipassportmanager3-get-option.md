---
description: Recupera o valor de uma opção de entrada específica do Microsoft .NET Passport.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'Método IPassportManager3:: get_Option'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370356"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="1539f-103">Método de opção IPassportManager3:: get \_</span><span class="sxs-lookup"><span data-stu-id="1539f-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="1539f-104">Recupera o valor de uma opção de entrada específica do Microsoft .NET Passport.</span><span class="sxs-lookup"><span data-stu-id="1539f-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="1539f-105">O método **Get \_ Option** pertence à interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="1539f-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="1539f-106">Este tópico complementa a documentação inicial.</span><span class="sxs-lookup"><span data-stu-id="1539f-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1539f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1539f-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1539f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1539f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1539f-109">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1539f-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1539f-110">A opção de entrada a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="1539f-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="1539f-111">Atualmente, a única opção com suporte é "iMode".</span><span class="sxs-lookup"><span data-stu-id="1539f-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="1539f-112">*PVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1539f-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1539f-113">Um ponteiro para uma **variante** (VT \_ bool) que recebe o valor da opção.</span><span class="sxs-lookup"><span data-stu-id="1539f-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="1539f-114">Esse valor pode ser true ou false.</span><span class="sxs-lookup"><span data-stu-id="1539f-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1539f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1539f-115">Return value</span></span>

<span data-ttu-id="1539f-116">Retorna S \_ OK quando o método for bem sucedido.</span><span class="sxs-lookup"><span data-stu-id="1539f-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="1539f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1539f-117">Remarks</span></span>

<span data-ttu-id="1539f-118">Esse método é fornecido com versões mais antigas do SDK do Passport.</span><span class="sxs-lookup"><span data-stu-id="1539f-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
