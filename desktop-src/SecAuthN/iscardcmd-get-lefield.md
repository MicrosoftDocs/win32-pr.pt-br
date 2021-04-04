---
description: Retorna o campo Le da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 249e8105-273b-42f0-9427-9b3cda5bf0a1
title: 'Método ISCardCmd:: get_LeField (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_LeField
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bc35f2686a32ce07e1ca630d3ccad3c47b36ca2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663359"
---
# <a name="iscardcmdget_lefield-method"></a><span data-ttu-id="90915-103">Método ISCardCmd:: get \_ LeField</span><span class="sxs-lookup"><span data-stu-id="90915-103">ISCardCmd::get\_LeField method</span></span>

<span data-ttu-id="90915-104">\[O método **Get \_ LeField** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="90915-104">\[The **get\_LeField** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="90915-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="90915-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="90915-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="90915-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="90915-107">O método **Get \_ LeField** retorna o campo Le da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="90915-107">The **get\_LeField** method returns the Le field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="90915-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90915-108">Syntax</span></span>


```C++
HRESULT get_LeField(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="90915-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90915-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90915-110">*plSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="90915-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90915-111">Ponteiro para o valor do campo Le no retorno.</span><span class="sxs-lookup"><span data-stu-id="90915-111">Pointer to the Le field value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90915-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90915-112">Return value</span></span>

<span data-ttu-id="90915-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="90915-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="90915-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="90915-114">Return code</span></span>                                                                                  | <span data-ttu-id="90915-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="90915-115">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="90915-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90915-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="90915-117">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="90915-117">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="90915-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="90915-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="90915-119">O parâmetro *plSize* não é válido.</span><span class="sxs-lookup"><span data-stu-id="90915-119">The *plSize* parameter is not valid.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="90915-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90915-120">Examples</span></span>

<span data-ttu-id="90915-121">O exemplo a seguir mostra como recuperar o valor do campo Le da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="90915-121">The following example shows how to retrieve the Le field value from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="90915-122">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="90915-122">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG     lLe;
HRESULT  hr;

// Retrieve the Le field value.
hr = pISCardCmd->get_LeField(&lLe);
if (FAILED(hr))
{
    printf("Failed get_LeField\n");
    // Take other error handling action.
}
else
    printf("Le field value returned is %d\n", lLe);
```



## <a name="requirements"></a><span data-ttu-id="90915-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90915-123">Requirements</span></span>



| <span data-ttu-id="90915-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="90915-124">Requirement</span></span> | <span data-ttu-id="90915-125">Valor</span><span class="sxs-lookup"><span data-stu-id="90915-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90915-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90915-126">Minimum supported client</span></span><br/> | <span data-ttu-id="90915-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="90915-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="90915-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90915-128">Minimum supported server</span></span><br/> | <span data-ttu-id="90915-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90915-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90915-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="90915-130">End of client support</span></span><br/>    | <span data-ttu-id="90915-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="90915-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="90915-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="90915-132">End of server support</span></span><br/>    | <span data-ttu-id="90915-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90915-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="90915-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90915-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="90915-135"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="90915-135"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="90915-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="90915-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="90915-137"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="90915-137"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="90915-138">DLL</span><span class="sxs-lookup"><span data-stu-id="90915-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90915-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90915-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="90915-140">IID</span><span class="sxs-lookup"><span data-stu-id="90915-140">IID</span></span><br/>                      | <span data-ttu-id="90915-141">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="90915-141">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="90915-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="90915-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90915-143">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="90915-143">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
