---
description: Define o campo de dados na APDU (unidade de dados do protocolo de aplicativo).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd: método de ut_Data de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090926"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="b5723-103">Método de dados ISCardCmd::p UT \_</span><span class="sxs-lookup"><span data-stu-id="b5723-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="b5723-104">\[O método **Put \_ Data** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b5723-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b5723-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b5723-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5723-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b5723-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b5723-107">O método **Put \_ Data** define o campo de dados na APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="b5723-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5723-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5723-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="b5723-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5723-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5723-110">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5723-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5723-111">Ponteiro para o **IStream**(objeto de buffer de bytes) a ser copiado para o campo de dados APDU.</span><span class="sxs-lookup"><span data-stu-id="b5723-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5723-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5723-112">Return value</span></span>

<span data-ttu-id="b5723-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b5723-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b5723-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5723-114">Return code</span></span>                                                                                   | <span data-ttu-id="b5723-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5723-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b5723-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b5723-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b5723-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="b5723-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b5723-119">O parâmetro *pData* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b5723-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b5723-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b5723-121">Um ponteiro inadequado foi passado em *pData*.</span><span class="sxs-lookup"><span data-stu-id="b5723-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="b5723-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b5723-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b5723-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b5723-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5723-124">Remarks</span></span>

<span data-ttu-id="b5723-125">Quando você define uma nova parte de dados da mensagem, o comprimento do campo de dados é calculado e armazenado no parâmetro P3 do APDU.</span><span class="sxs-lookup"><span data-stu-id="b5723-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="b5723-126">Para recuperar o comprimento do campo de dados, chame [**Get \_ P3**](iscardcmd-get-p3.md).</span><span class="sxs-lookup"><span data-stu-id="b5723-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="b5723-127">Para recuperar o campo de dados do APDU, chame [**obter \_ dados**](iscardcmd-get-data.md).</span><span class="sxs-lookup"><span data-stu-id="b5723-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b5723-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5723-128">Examples</span></span>

<span data-ttu-id="b5723-129">O exemplo a seguir mostra como definir o campo de dados na [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="b5723-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="b5723-130">O exemplo supõe que pIByteData é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="b5723-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="b5723-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5723-131">Requirements</span></span>



| <span data-ttu-id="b5723-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5723-132">Requirement</span></span> | <span data-ttu-id="b5723-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b5723-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5723-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5723-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5723-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5723-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b5723-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5723-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5723-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5723-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5723-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b5723-138">End of client support</span></span><br/>    | <span data-ttu-id="b5723-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5723-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b5723-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b5723-140">End of server support</span></span><br/>    | <span data-ttu-id="b5723-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5723-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b5723-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5723-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5723-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5723-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b5723-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5723-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5723-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b5723-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5723-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5723-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5723-148">IID</span><span class="sxs-lookup"><span data-stu-id="b5723-148">IID</span></span><br/>                      | <span data-ttu-id="b5723-149">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b5723-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b5723-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5723-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5723-151">**obter \_ dados**</span><span class="sxs-lookup"><span data-stu-id="b5723-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="b5723-152">**obter \_ P3**</span><span class="sxs-lookup"><span data-stu-id="b5723-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="b5723-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="b5723-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
