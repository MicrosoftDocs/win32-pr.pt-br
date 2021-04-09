---
description: O método Write grava dados em um arquivo aberto atual.
ms.assetid: 0c92af34-a9db-4242-8b6e-d1010a0d7afa
title: 'Método ISCardFileAccess:: Write'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 48091d39fff49e54d57f5a26fb7d033bfd8e5952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091523"
---
# <a name="iscardfileaccesswrite-method"></a><span data-ttu-id="1ef64-103">Método ISCardFileAccess:: Write</span><span class="sxs-lookup"><span data-stu-id="1ef64-103">ISCardFileAccess::Write method</span></span>

<span data-ttu-id="1ef64-104">\[O método **Write** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1ef64-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ef64-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1ef64-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1ef64-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1ef64-107">O método **Write** grava dados em um arquivo aberto atual.</span><span class="sxs-lookup"><span data-stu-id="1ef64-107">The **Write** method writes data to a current opened file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef64-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ef64-108">Syntax</span></span>


```C++
HRESULT Write(
  [in] HSCARD_FILE  hFile,
  [in] LPBYTEBUFFER pData,
  [in] SCARD_FLAGS  flags
);
```



## <a name="parameters"></a><span data-ttu-id="1ef64-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ef64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef64-110">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef64-111">Um identificador para um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="1ef64-111">A handle to an open file.</span></span>

</dd> <dt>

<span data-ttu-id="1ef64-112">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef64-113">Objeto/dados a serem gravados.</span><span class="sxs-lookup"><span data-stu-id="1ef64-113">Object/data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="1ef64-114">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef64-115">Especifica se as mensagens seguras devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="1ef64-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="1ef64-116">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="1ef64-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef64-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ef64-117">Return value</span></span>

<span data-ttu-id="1ef64-118">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="1ef64-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1ef64-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1ef64-119">Return code</span></span>                                                                                   | <span data-ttu-id="1ef64-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ef64-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1ef64-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef64-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1ef64-122">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1ef64-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1ef64-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef64-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1ef64-124">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="1ef64-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1ef64-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef64-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1ef64-126">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="1ef64-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1ef64-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1ef64-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1ef64-128">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="1ef64-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1ef64-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ef64-129">Remarks</span></span>

<span data-ttu-id="1ef64-130">Para abrir ou fechar um arquivo, chame [**Open**](iscardfileaccess-open.md) ou [**Close**](iscardfileaccess-close.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1ef64-130">To open or close a file, call [**Open**](iscardfileaccess-open.md) or [**Close**](iscardfileaccess-close.md), respectively.</span></span>

<span data-ttu-id="1ef64-131">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="1ef64-131">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="1ef64-132">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="1ef64-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1ef64-133">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1ef64-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef64-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ef64-134">Requirements</span></span>



| <span data-ttu-id="1ef64-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef64-135">Requirement</span></span> | <span data-ttu-id="1ef64-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1ef64-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ef64-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef64-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef64-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1ef64-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef64-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef64-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ef64-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ef64-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1ef64-141">End of client support</span></span><br/>    | <span data-ttu-id="1ef64-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ef64-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="1ef64-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1ef64-143">End of server support</span></span><br/>    | <span data-ttu-id="1ef64-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ef64-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1ef64-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ef64-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef64-146">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="1ef64-146">**Close**</span></span>](iscardfileaccess-close.md)
</dt> <dt>

[<span data-ttu-id="1ef64-147">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="1ef64-147">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="1ef64-148">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="1ef64-148">**Open**</span></span>](iscardfileaccess-open.md)
</dt> </dl>

 

 
