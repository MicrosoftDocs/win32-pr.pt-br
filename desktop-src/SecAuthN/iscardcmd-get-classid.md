---
description: Recupera o identificador de classe da APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Método ISCardCmd:: get_ClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090469"
---
# <a name="iscardcmdget_classid-method"></a><span data-ttu-id="8d341-103">Método ISCardCmd:: get \_ ClassID</span><span class="sxs-lookup"><span data-stu-id="8d341-103">ISCardCmd::get\_ClassId method</span></span>

<span data-ttu-id="8d341-104">\[O método **Get \_ ClassID** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8d341-104">\[The **get\_ClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8d341-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8d341-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8d341-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8d341-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8d341-107">O método **Get \_ ClassID** recupera o identificador de classe da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="8d341-107">The **get\_ClassId** method retrieves the class identifier from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d341-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d341-108">Syntax</span></span>


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a><span data-ttu-id="8d341-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d341-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d341-110">*pbyClass* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d341-110">*pbyClass* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d341-111">Ponteiro para o byte que representa o identificador de classe.</span><span class="sxs-lookup"><span data-stu-id="8d341-111">Pointer to the byte that represents the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d341-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d341-112">Return value</span></span>

<span data-ttu-id="8d341-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8d341-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8d341-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8d341-114">Return code</span></span>                                                                                   | <span data-ttu-id="8d341-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d341-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8d341-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8d341-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8d341-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="8d341-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8d341-119">O parâmetro *pbyClass* não é válido.</span><span class="sxs-lookup"><span data-stu-id="8d341-119">The *pbyClass* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="8d341-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8d341-121">Um ponteiro inadequado foi passado em *pbyClass*.</span><span class="sxs-lookup"><span data-stu-id="8d341-121">A bad pointer was passed in *pbyClass*.</span></span><br/> |
| <dl> <span data-ttu-id="8d341-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8d341-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="8d341-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8d341-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d341-124">Remarks</span></span>

<span data-ttu-id="8d341-125">Para definir o identificador de classe como um novo valor, chame [**Put \_ ClassID**](iscardcmd-put-classid.md).</span><span class="sxs-lookup"><span data-stu-id="8d341-125">To set the class identifier to a new value, call [**put\_ClassId**](iscardcmd-put-classid.md).</span></span>

<span data-ttu-id="8d341-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="8d341-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="8d341-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8d341-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8d341-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8d341-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8d341-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d341-129">Examples</span></span>

<span data-ttu-id="8d341-130">O exemplo a seguir mostra como recuperar a ID de classe.</span><span class="sxs-lookup"><span data-stu-id="8d341-130">The following example shows how to retrieve the class ID.</span></span> <span data-ttu-id="8d341-131">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="8d341-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="8d341-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d341-132">Requirements</span></span>



| <span data-ttu-id="8d341-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d341-133">Requirement</span></span> | <span data-ttu-id="8d341-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8d341-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d341-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d341-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8d341-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d341-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8d341-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d341-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8d341-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d341-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d341-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8d341-139">End of client support</span></span><br/>    | <span data-ttu-id="8d341-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d341-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8d341-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8d341-141">End of server support</span></span><br/>    | <span data-ttu-id="8d341-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d341-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8d341-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d341-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d341-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d341-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8d341-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d341-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d341-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8d341-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d341-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d341-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8d341-149">IID</span><span class="sxs-lookup"><span data-stu-id="8d341-149">IID</span></span><br/>                      | <span data-ttu-id="8d341-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8d341-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="8d341-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d341-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d341-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="8d341-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="8d341-153">**colocar \_ ClassID**</span><span class="sxs-lookup"><span data-stu-id="8d341-153">**put\_ClassId**</span></span>](iscardcmd-put-classid.md)
</dt> </dl>

 

 
