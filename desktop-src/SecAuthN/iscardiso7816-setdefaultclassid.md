---
description: O método SetDefaultClassId atribui um byte de identificador de classe padrão que será usado em todas as operações ao construir uma APDU (unidade de dados do protocolo de aplicativo de comando) ISO 7816-4. Por padrão, o byte do identificador de classe padrão é 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: 'Método ISCardISO7816:: SetDefaultClassId (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 29e8868f491f0b9a61554da008c4100622815dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752749"
---
# <a name="iscardiso7816setdefaultclassid-method"></a><span data-ttu-id="92d6e-104">Método ISCardISO7816:: SetDefaultClassId</span><span class="sxs-lookup"><span data-stu-id="92d6e-104">ISCardISO7816::SetDefaultClassId method</span></span>

<span data-ttu-id="92d6e-105">\[O método **SetDefaultClassId** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="92d6e-105">\[The **SetDefaultClassId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="92d6e-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="92d6e-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="92d6e-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="92d6e-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="92d6e-108">O método **SetDefaultClassId** atribui um byte de identificador de classe padrão que será usado em todas as operações ao construir uma APDU (unidade de [*dados do protocolo de aplicativo*](../secgloss/a-gly.md) de comando) ISO 7816-4.</span><span class="sxs-lookup"><span data-stu-id="92d6e-108">The **SetDefaultClassId** method assigns a standard class identifier byte that will be used in all operations when constructing an ISO 7816-4 command [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="92d6e-109">Por padrão, o byte do identificador de classe padrão é 0x00.</span><span class="sxs-lookup"><span data-stu-id="92d6e-109">By default, the standard class identifier byte is 0x00.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d6e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92d6e-110">Syntax</span></span>


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a><span data-ttu-id="92d6e-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92d6e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92d6e-112">*byClass* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92d6e-112">*byClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92d6e-113">Byte de ID de classe.</span><span class="sxs-lookup"><span data-stu-id="92d6e-113">Class ID byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92d6e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92d6e-114">Return value</span></span>

<span data-ttu-id="92d6e-115">Os possíveis valores de retorno são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="92d6e-115">The possible return values are the following:</span></span>



| <span data-ttu-id="92d6e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="92d6e-116">Return code</span></span>                                                                          | <span data-ttu-id="92d6e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="92d6e-117">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="92d6e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92d6e-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="92d6e-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="92d6e-119">Operation completed successfully.</span></span><br/> |



 

<span data-ttu-id="92d6e-120">Para obter uma lista de todos os métodos fornecidos pela interface [**ISCardISO7816**](iscardiso7816.md) , consulte **ISCardISO7816**.</span><span class="sxs-lookup"><span data-stu-id="92d6e-120">For a list of all the methods provided by the [**ISCardISO7816**](iscardiso7816.md) interface, see **ISCardISO7816**.</span></span>

<span data-ttu-id="92d6e-121">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="92d6e-121">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="92d6e-122">Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="92d6e-122">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92d6e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d6e-123">Requirements</span></span>



| <span data-ttu-id="92d6e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d6e-124">Requirement</span></span> | <span data-ttu-id="92d6e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="92d6e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92d6e-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92d6e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="92d6e-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="92d6e-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92d6e-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92d6e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="92d6e-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="92d6e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92d6e-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="92d6e-130">End of client support</span></span><br/>    | <span data-ttu-id="92d6e-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="92d6e-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="92d6e-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="92d6e-132">End of server support</span></span><br/>    | <span data-ttu-id="92d6e-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92d6e-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="92d6e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92d6e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="92d6e-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92d6e-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="92d6e-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="92d6e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="92d6e-137"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="92d6e-137"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="92d6e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="92d6e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92d6e-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92d6e-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="92d6e-140">IID</span><span class="sxs-lookup"><span data-stu-id="92d6e-140">IID</span></span><br/>                      | <span data-ttu-id="92d6e-141">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="92d6e-141">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="92d6e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="92d6e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d6e-143">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="92d6e-143">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
