---
description: Especifica um novo identificador de classe alternativo na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: 'ISCardCmd: método de ut_AlternateClassId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747931"
---
# <a name="iscardcmdput_alternateclassid-method"></a><span data-ttu-id="0f33c-103">ISCardCmd: método UT \_ AlternateClassId:p</span><span class="sxs-lookup"><span data-stu-id="0f33c-103">ISCardCmd::put\_AlternateClassId method</span></span>

<span data-ttu-id="0f33c-104">\[O método **Put \_ AlternateClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="0f33c-104">\[The **put\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f33c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0f33c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0f33c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="0f33c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0f33c-107">O método **Put \_ AlternateClassId** especifica um novo identificador de classe alternativo na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="0f33c-107">The **put\_AlternateClassId** method specifies a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f33c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f33c-108">Syntax</span></span>


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="0f33c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f33c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f33c-110">*byClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f33c-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f33c-111">Identificador de classe alternativo.</span><span class="sxs-lookup"><span data-stu-id="0f33c-111">Alternate class identifier.</span></span> <span data-ttu-id="0f33c-112">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="0f33c-112">The default value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f33c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f33c-113">Return value</span></span>

<span data-ttu-id="0f33c-114">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0f33c-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0f33c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f33c-115">Return code</span></span>                                                                                  | <span data-ttu-id="0f33c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f33c-116">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0f33c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f33c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0f33c-118">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="0f33c-118">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="0f33c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0f33c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0f33c-120">O parâmetro *byClass* não é válido.</span><span class="sxs-lookup"><span data-stu-id="0f33c-120">The *byClass* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f33c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f33c-121">Remarks</span></span>

<span data-ttu-id="0f33c-122">Com as comunicações usando o [*protocolo T = 0*](../secgloss/t-gly.md), comandos de cartão adicionais podem ser gerados automaticamente pelo APDU e enviados para a unidade de dados do protocolo de transmissão (TPDU).</span><span class="sxs-lookup"><span data-stu-id="0f33c-122">With communications using the [*T=0 protocol*](../secgloss/t-gly.md), additional card commands can be automatically generated by the APDU and sent to the transmission protocol data unit (TPDU).</span></span> <span data-ttu-id="0f33c-123">Os comandos adicionais normalmente usam a mesma ID de classe que o comando original; a especificação de uma nova ID de classe por meio desse método permite que comandos gerados automaticamente usem a nova ID de classe.</span><span class="sxs-lookup"><span data-stu-id="0f33c-123">The additional commands typically use the same class ID as the original command; specifying a new class ID by means of this method allows automatically generated commands to use the new class ID.</span></span>

## <a name="examples"></a><span data-ttu-id="0f33c-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f33c-124">Examples</span></span>

<span data-ttu-id="0f33c-125">O exemplo a seguir mostra como definir um novo identificador de classe alternativo na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="0f33c-125">The following example shows how to set a new alternate class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="0f33c-126">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="0f33c-126">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="0f33c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f33c-127">Requirements</span></span>



| <span data-ttu-id="0f33c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f33c-128">Requirement</span></span> | <span data-ttu-id="0f33c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0f33c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f33c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f33c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0f33c-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0f33c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0f33c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f33c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0f33c-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f33c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0f33c-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0f33c-134">End of client support</span></span><br/>    | <span data-ttu-id="0f33c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0f33c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0f33c-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0f33c-136">End of server support</span></span><br/>    | <span data-ttu-id="0f33c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f33c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0f33c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f33c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f33c-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f33c-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f33c-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0f33c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f33c-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f33c-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f33c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0f33c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f33c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f33c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f33c-144">IID</span><span class="sxs-lookup"><span data-stu-id="0f33c-144">IID</span></span><br/>                      | <span data-ttu-id="0f33c-145">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0f33c-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0f33c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f33c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f33c-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="0f33c-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="0f33c-148">**obter \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="0f33c-148">**get\_AlternateClassId**</span></span>](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
