---
description: Especifica o endereço do nó (NAD) a ser usado com a interface ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: método de ut_Nad de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827462"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="726c9-103">Método ISCardCmd::p UT \_ nad</span><span class="sxs-lookup"><span data-stu-id="726c9-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="726c9-104">\[O método do **\_ nad Put** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="726c9-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="726c9-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="726c9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="726c9-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="726c9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="726c9-107">O método da **\_ nad Put** especifica o endereço do nó (NAD) a ser usado com a interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="726c9-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="726c9-108">Isso se aplica às comunicações usando apenas as comunicações de [*protocolo T = 1*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="726c9-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="726c9-109">Por padrão, o objeto [**ISCardCmd**](iscardcmd.md) usa um nad de zero.</span><span class="sxs-lookup"><span data-stu-id="726c9-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="726c9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="726c9-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="726c9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="726c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726c9-112">*bNad* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="726c9-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="726c9-113">Byte que representa o NAD a ser usado.</span><span class="sxs-lookup"><span data-stu-id="726c9-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726c9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="726c9-114">Return value</span></span>

<span data-ttu-id="726c9-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="726c9-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="726c9-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="726c9-116">Return code</span></span>                                                                                  | <span data-ttu-id="726c9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="726c9-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="726c9-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="726c9-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="726c9-119">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="726c9-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="726c9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="726c9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="726c9-121">O parâmetro *bNad* não é válido.</span><span class="sxs-lookup"><span data-stu-id="726c9-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="726c9-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="726c9-122">Remarks</span></span>

<span data-ttu-id="726c9-123">Esse método deve ser chamado somente quando for necessário usar um valor diferente de zero para o NAD.</span><span class="sxs-lookup"><span data-stu-id="726c9-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="726c9-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="726c9-124">Examples</span></span>

<span data-ttu-id="726c9-125">O exemplo a seguir mostra como especificar um endereço de nó para usar com a interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="726c9-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="726c9-126">O exemplo supõe que byNadValue é uma variável do tipo **byte** que anteriormente atribuiu um valor e que pISCardCmd é um ponteiro válido para uma instância da interface **ISCardCmd** .</span><span class="sxs-lookup"><span data-stu-id="726c9-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="726c9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726c9-127">Requirements</span></span>



| <span data-ttu-id="726c9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="726c9-128">Requirement</span></span> | <span data-ttu-id="726c9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="726c9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="726c9-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726c9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="726c9-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="726c9-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="726c9-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="726c9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="726c9-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="726c9-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="726c9-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="726c9-134">End of client support</span></span><br/>    | <span data-ttu-id="726c9-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="726c9-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="726c9-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="726c9-136">End of server support</span></span><br/>    | <span data-ttu-id="726c9-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="726c9-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="726c9-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726c9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="726c9-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="726c9-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="726c9-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="726c9-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="726c9-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="726c9-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="726c9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="726c9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="726c9-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726c9-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="726c9-144">IID</span><span class="sxs-lookup"><span data-stu-id="726c9-144">IID</span></span><br/>                      | <span data-ttu-id="726c9-145">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="726c9-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="726c9-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="726c9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726c9-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="726c9-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
