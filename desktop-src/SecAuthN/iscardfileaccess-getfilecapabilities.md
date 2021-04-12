---
description: O método GetFileCapabilities recupera uma lista de recursos de arquivo do arquivo atual.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Método ISCardFileAccess:: GetFileCapabilities'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170217"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="35cbb-103">Método ISCardFileAccess:: GetFileCapabilities</span><span class="sxs-lookup"><span data-stu-id="35cbb-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="35cbb-104">\[O método **GetFileCapabilities** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="35cbb-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="35cbb-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="35cbb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="35cbb-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="35cbb-107">O método **GetFileCapabilities** recupera uma lista de recursos de arquivo do arquivo atual.</span><span class="sxs-lookup"><span data-stu-id="35cbb-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="35cbb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35cbb-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="35cbb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35cbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35cbb-110">*ppProperties* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35cbb-111">Ponteiro para estruturas TLV (marca, comprimento, valor).</span><span class="sxs-lookup"><span data-stu-id="35cbb-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="35cbb-112">Na entrada, esse parâmetro indica os arquivos para os quais obter propriedades; na saída, esse parâmetro contém as propriedades.</span><span class="sxs-lookup"><span data-stu-id="35cbb-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="35cbb-113">O exemplo a seguir é uma definição da estrutura TLV.</span><span class="sxs-lookup"><span data-stu-id="35cbb-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="35cbb-114">Para obter mais informações sobre estruturas TLV, consulte [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="35cbb-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="35cbb-115">*plProperties* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35cbb-116">Ponteiro para o número de entradas TLV em *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="35cbb-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="35cbb-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35cbb-118">Especifica se as mensagens seguras devem ser usadas e os dados alocados.</span><span class="sxs-lookup"><span data-stu-id="35cbb-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="35cbb-119">**\_ \_ mensagens seguras do SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="35cbb-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="35cbb-120">**SC \_ fl \_ prealocado**</span><span class="sxs-lookup"><span data-stu-id="35cbb-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35cbb-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35cbb-121">Return value</span></span>

<span data-ttu-id="35cbb-122">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="35cbb-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="35cbb-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="35cbb-123">Return code</span></span>                                                                                   | <span data-ttu-id="35cbb-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="35cbb-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="35cbb-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35cbb-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="35cbb-126">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="35cbb-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="35cbb-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="35cbb-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="35cbb-128">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="35cbb-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="35cbb-129"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="35cbb-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="35cbb-130">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="35cbb-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="35cbb-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="35cbb-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="35cbb-132">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="35cbb-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="35cbb-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="35cbb-133">Remarks</span></span>

<span data-ttu-id="35cbb-134">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="35cbb-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="35cbb-135">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="35cbb-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="35cbb-136">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="35cbb-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35cbb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35cbb-137">Requirements</span></span>



| <span data-ttu-id="35cbb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="35cbb-138">Requirement</span></span> | <span data-ttu-id="35cbb-139">Valor</span><span class="sxs-lookup"><span data-stu-id="35cbb-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35cbb-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35cbb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="35cbb-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="35cbb-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35cbb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="35cbb-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35cbb-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="35cbb-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="35cbb-144">End of client support</span></span><br/>    | <span data-ttu-id="35cbb-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="35cbb-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="35cbb-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="35cbb-146">End of server support</span></span><br/>    | <span data-ttu-id="35cbb-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="35cbb-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="35cbb-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="35cbb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35cbb-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="35cbb-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
