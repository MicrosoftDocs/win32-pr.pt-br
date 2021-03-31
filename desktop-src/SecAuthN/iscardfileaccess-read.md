---
description: O método Read lê e retorna os dados especificados de um determinado arquivo.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'Método ISCardFileAccess:: Read'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169701"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="a526d-103">Método ISCardFileAccess:: Read</span><span class="sxs-lookup"><span data-stu-id="a526d-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="a526d-104">\[O método **Read** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a526d-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a526d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a526d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a526d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a526d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a526d-107">O método **Read** lê e retorna os dados especificados de um determinado arquivo.</span><span class="sxs-lookup"><span data-stu-id="a526d-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a526d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a526d-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="a526d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a526d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a526d-110">*hFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a526d-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a526d-111">Identificador do arquivo aberto a ser acessado.</span><span class="sxs-lookup"><span data-stu-id="a526d-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="a526d-112">*lBytesToRead* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a526d-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a526d-113">Comprimento dos dados a serem lidos (em) ou número de bytes lidos (out).</span><span class="sxs-lookup"><span data-stu-id="a526d-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="a526d-114">Retorna a lista de arquivos como uma matriz de BSTRs.</span><span class="sxs-lookup"><span data-stu-id="a526d-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="a526d-115">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a526d-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a526d-116">Especifica se as mensagens seguras devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="a526d-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="a526d-117">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="a526d-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a526d-118">*ppBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a526d-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a526d-119">Um objeto [**IByteBuffer**](ibytebuffer.md) que contém os dados de leitura.</span><span class="sxs-lookup"><span data-stu-id="a526d-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a526d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a526d-120">Return value</span></span>

<span data-ttu-id="a526d-121">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a526d-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a526d-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a526d-122">Return code</span></span>                                                                                   | <span data-ttu-id="a526d-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="a526d-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a526d-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a526d-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a526d-125">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a526d-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a526d-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a526d-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a526d-127">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="a526d-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a526d-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a526d-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a526d-129">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="a526d-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a526d-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a526d-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a526d-131">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a526d-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a526d-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a526d-132">Remarks</span></span>

<span data-ttu-id="a526d-133">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="a526d-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="a526d-134">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a526d-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a526d-135">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a526d-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a526d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a526d-136">Requirements</span></span>



| <span data-ttu-id="a526d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a526d-137">Requirement</span></span> | <span data-ttu-id="a526d-138">Valor</span><span class="sxs-lookup"><span data-stu-id="a526d-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a526d-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a526d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a526d-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a526d-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a526d-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a526d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a526d-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a526d-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a526d-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a526d-143">End of client support</span></span><br/>    | <span data-ttu-id="a526d-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a526d-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a526d-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a526d-145">End of server support</span></span><br/>    | <span data-ttu-id="a526d-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a526d-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="a526d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a526d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a526d-148">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="a526d-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
