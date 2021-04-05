---
description: Define um novo identificador de classe na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 7e7d42f2-2858-4b37-a7d5-a919e3e005da
title: 'ISCardCmd: método de ut_ClassId de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ed4b1f273ebe9ea0a5e105ec3d88fc8446f7a831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921153"
---
# <a name="iscardcmdput_classid-method"></a><span data-ttu-id="798a9-103">Método ISCardCmd::p UT \_ ClassID</span><span class="sxs-lookup"><span data-stu-id="798a9-103">ISCardCmd::put\_ClassId method</span></span>

<span data-ttu-id="798a9-104">\[O método **Put \_ ClassID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="798a9-104">\[The **put\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="798a9-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="798a9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="798a9-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="798a9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="798a9-107">O método **Put \_ ClassID** define um novo identificador de classe na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="798a9-107">The **put\_ClassId** method sets a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="798a9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="798a9-108">Syntax</span></span>


```C++
HRESULT put_ClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="798a9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="798a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798a9-110">*byClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="798a9-110">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798a9-111">O byte que representa o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="798a9-111">The byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798a9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="798a9-112">Return value</span></span>

<span data-ttu-id="798a9-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="798a9-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="798a9-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="798a9-114">Return code</span></span>                                                                                   | <span data-ttu-id="798a9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="798a9-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="798a9-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="798a9-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="798a9-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="798a9-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="798a9-119">O *byClass* não é válido.</span><span class="sxs-lookup"><span data-stu-id="798a9-119">The *byClass* is not valid.</span></span><br/>       |
| <dl> <span data-ttu-id="798a9-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="798a9-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="798a9-121">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="798a9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="798a9-122">Remarks</span></span>

<span data-ttu-id="798a9-123">Para recuperar o identificador de classe atual, chame [**Get \_ ClassID**](iscardcmd-get-classid.md).</span><span class="sxs-lookup"><span data-stu-id="798a9-123">To retrieve the current class identifier, call [**get\_ClassId**](iscardcmd-get-classid.md).</span></span>

<span data-ttu-id="798a9-124">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="798a9-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="798a9-125">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="798a9-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="798a9-126">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="798a9-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="798a9-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="798a9-127">Examples</span></span>

<span data-ttu-id="798a9-128">O exemplo a seguir mostra como definir um novo identificador de classe na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="798a9-128">The following example shows how to set a new class identifier in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="798a9-129">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="798a9-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_ClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="798a9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="798a9-130">Requirements</span></span>



| <span data-ttu-id="798a9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="798a9-131">Requirement</span></span> | <span data-ttu-id="798a9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="798a9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="798a9-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798a9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="798a9-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="798a9-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="798a9-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798a9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="798a9-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="798a9-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="798a9-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="798a9-137">End of client support</span></span><br/>    | <span data-ttu-id="798a9-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="798a9-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="798a9-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="798a9-139">End of server support</span></span><br/>    | <span data-ttu-id="798a9-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="798a9-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="798a9-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="798a9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="798a9-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="798a9-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="798a9-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="798a9-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="798a9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="798a9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="798a9-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="798a9-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="798a9-147">IID</span><span class="sxs-lookup"><span data-stu-id="798a9-147">IID</span></span><br/>                      | <span data-ttu-id="798a9-148">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="798a9-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="798a9-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="798a9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="798a9-150">**obter \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="798a9-150">**get\_ClassId**</span></span>](iscardcmd-get-classid.md)
</dt> <dt>

[<span data-ttu-id="798a9-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="798a9-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
