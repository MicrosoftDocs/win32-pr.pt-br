---
description: Recupera o valor da ID de classe alternativa.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Método ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748466"
---
# <a name="iscardcmdget_alternateclassid-method"></a><span data-ttu-id="0a86d-103">Método ISCardCmd:: get \_ AlternateClassId</span><span class="sxs-lookup"><span data-stu-id="0a86d-103">ISCardCmd::get\_AlternateClassId method</span></span>

<span data-ttu-id="0a86d-104">\[O método **Get \_ AlternateClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="0a86d-104">\[The **get\_AlternateClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0a86d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0a86d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0a86d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="0a86d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0a86d-107">O método **Get \_ AlternateClassId** recupera o valor da ID de classe alternativa.</span><span class="sxs-lookup"><span data-stu-id="0a86d-107">The **get\_AlternateClassId** method retrieves the value of the alternate class ID.</span></span> <span data-ttu-id="0a86d-108">Esse método falhará a menos que a ID alternativa tenha sido definida por uma chamada anterior para [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="0a86d-108">This method will fail unless the alternate ID has been set by a previous call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a86d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a86d-109">Syntax</span></span>


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="0a86d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a86d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a86d-111">*pbyClass* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a86d-111">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a86d-112">Ponteiro para o byte que contém o valor de ID de classe alternativo no retorno.</span><span class="sxs-lookup"><span data-stu-id="0a86d-112">Pointer to the byte that contains the alternate class ID value on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a86d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a86d-113">Return value</span></span>

<span data-ttu-id="0a86d-114">O método retorna os seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="0a86d-114">The method returns the following possible values.</span></span>



| <span data-ttu-id="0a86d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0a86d-115">Return code</span></span>                                                                                    | <span data-ttu-id="0a86d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a86d-116">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a86d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="0a86d-118">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="0a86d-118">Operation was completed successfully.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="0a86d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="0a86d-120">O parâmetro *pbyClass* não é válido.</span><span class="sxs-lookup"><span data-stu-id="0a86d-120">The *pbyClass* parameter is not valid.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="0a86d-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="0a86d-122">A ID de classe alternativa não foi definida anteriormente por uma chamada para [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="0a86d-122">The alternate class ID has not been previously set by a call to [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0a86d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a86d-123">Remarks</span></span>

<span data-ttu-id="0a86d-124">Esse método se aplica a comunicações usando o [*protocolo T = 0*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0a86d-124">This method applies to communications using the [*T=0 protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="0a86d-125">Para obter mais informações, consulte [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).</span><span class="sxs-lookup"><span data-stu-id="0a86d-125">For more information, see [**put\_AlternateClassId**](iscardcmd-put-alternateclassid.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0a86d-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0a86d-126">Examples</span></span>

<span data-ttu-id="0a86d-127">O exemplo a seguir mostra como recuperar a ID de classe alternativa.</span><span class="sxs-lookup"><span data-stu-id="0a86d-127">The following example shows how to retrieve the alternate class ID.</span></span> <span data-ttu-id="0a86d-128">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="0a86d-128">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="0a86d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a86d-129">Requirements</span></span>



| <span data-ttu-id="0a86d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a86d-130">Requirement</span></span> | <span data-ttu-id="0a86d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0a86d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a86d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a86d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0a86d-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0a86d-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0a86d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a86d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0a86d-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a86d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a86d-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0a86d-136">End of client support</span></span><br/>    | <span data-ttu-id="0a86d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a86d-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0a86d-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0a86d-138">End of server support</span></span><br/>    | <span data-ttu-id="0a86d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a86d-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0a86d-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a86d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a86d-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a86d-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a86d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a86d-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a86d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0a86d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a86d-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a86d-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a86d-146">IID</span><span class="sxs-lookup"><span data-stu-id="0a86d-146">IID</span></span><br/>                      | <span data-ttu-id="0a86d-147">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0a86d-147">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0a86d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a86d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a86d-149">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="0a86d-149">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="0a86d-150">**colocar \_ AlternateClassId**</span><span class="sxs-lookup"><span data-stu-id="0a86d-150">**put\_AlternateClassId**</span></span>](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
