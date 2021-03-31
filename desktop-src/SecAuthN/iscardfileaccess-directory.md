---
description: O método de diretório recupera uma lista de arquivos do tipo especificado do diretório atual.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: 'ISCardFileAccess: método diretório de:D'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827854"
---
# <a name="iscardfileaccessdirectory-method"></a><span data-ttu-id="535ca-103">ISCardFileAccess: método diretório de:D</span><span class="sxs-lookup"><span data-stu-id="535ca-103">ISCardFileAccess::Directory method</span></span>

<span data-ttu-id="535ca-104">\[O método de **diretório** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="535ca-104">\[The **Directory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="535ca-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="535ca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="535ca-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="535ca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="535ca-107">O método de **diretório** recupera uma lista de arquivos do tipo especificado do diretório atual.</span><span class="sxs-lookup"><span data-stu-id="535ca-107">The **Directory** method retrieves a list of files of the specified type from the current directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="535ca-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="535ca-108">Syntax</span></span>


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a><span data-ttu-id="535ca-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="535ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="535ca-110">*filetype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="535ca-110">*fileType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535ca-111">Tipo de arquivos de [*cartão inteligente*](../secgloss/s-gly.md) a serem listados.</span><span class="sxs-lookup"><span data-stu-id="535ca-111">Type of [*smart card*](../secgloss/s-gly.md) files to list.</span></span>



| <span data-ttu-id="535ca-112">Valor</span><span class="sxs-lookup"><span data-stu-id="535ca-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="535ca-113">Significado</span><span class="sxs-lookup"><span data-stu-id="535ca-113">Meaning</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <span data-ttu-id="535ca-114"><dt>**\_diretórios do tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-114"><dt>**SC\_TYPE\_DIRECTORIES**</dt></span></span> </dl>           | <span data-ttu-id="535ca-115">Listar somente arquivos de diretório.</span><span class="sxs-lookup"><span data-stu-id="535ca-115">List directory files only.</span></span><br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <span data-ttu-id="535ca-116"><dt>**\_arquivos do tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-116"><dt>**SC\_TYPE\_FILES**</dt></span></span> </dl>                             | <span data-ttu-id="535ca-117">Listar somente arquivos elementares.</span><span class="sxs-lookup"><span data-stu-id="535ca-117">List elementary files only.</span></span><br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <span data-ttu-id="535ca-118"><dt>**SC \_ digite \_ todos os \_ arquivos**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-118"><dt>**SC\_TYPE\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="535ca-119">Listar os arquivos de diretório e elementares.</span><span class="sxs-lookup"><span data-stu-id="535ca-119">List both directory and elementary files.</span></span><br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <span data-ttu-id="535ca-120"><dt>**\_arquivo de \_ diretório do tipo SC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-120"><dt>**SC\_TYPE\_DIRECTORY\_FILE**</dt></span></span> </dl> | <span data-ttu-id="535ca-121">Arquivo de diretório.</span><span class="sxs-lookup"><span data-stu-id="535ca-121">Directory file.</span></span><br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <span data-ttu-id="535ca-122"><dt>**SC \_ tipo \_ transparente \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-122"><dt>**SC\_TYPE\_TRANSPARENT\_EF**</dt></span></span> </dl> | <span data-ttu-id="535ca-123">Arquivo elementar transparente.</span><span class="sxs-lookup"><span data-stu-id="535ca-123">Transparent elementary file.</span></span><br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <span data-ttu-id="535ca-124"><dt>**\_tipo SC \_ Fixed \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-124"><dt>**SC\_TYPE\_FIXED\_EF**</dt></span></span> </dl>                   | <span data-ttu-id="535ca-125">Arquivo elementar fixo linear.</span><span class="sxs-lookup"><span data-stu-id="535ca-125">Linear fixed elementary file.</span></span><br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <span data-ttu-id="535ca-126"><dt>**SC \_ tipo \_ cíclico de \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-126"><dt>**SC\_TYPE\_CYCLIC\_EF**</dt></span></span> </dl>                | <span data-ttu-id="535ca-127">Arquivo de elementar cíclico.</span><span class="sxs-lookup"><span data-stu-id="535ca-127">Cyclic elementary file.</span></span><br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <span data-ttu-id="535ca-128"><dt>**SC \_ Type \_ variável \_ EF**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-128"><dt>**SC\_TYPE\_VARIABLE\_EF**</dt></span></span> </dl>          | <span data-ttu-id="535ca-129">Arquivo elementar variável linear.</span><span class="sxs-lookup"><span data-stu-id="535ca-129">Linear variable elementary file.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="535ca-130">*ppFileList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="535ca-130">*ppFileList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="535ca-131">Matriz de BSTRs que representa a lista de arquivos que correspondem ao especificador em *filetype*.</span><span class="sxs-lookup"><span data-stu-id="535ca-131">Array of BSTRs representing the list of files matching the specifier in *fileType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="535ca-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="535ca-132">Return value</span></span>

<span data-ttu-id="535ca-133">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="535ca-133">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="535ca-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="535ca-134">Return code</span></span>                                                                                   | <span data-ttu-id="535ca-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="535ca-135">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="535ca-136"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-136"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="535ca-137">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="535ca-137">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="535ca-138"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-138"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="535ca-139">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="535ca-139">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="535ca-140"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-140"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="535ca-141">A interface não implementou este método.</span><span class="sxs-lookup"><span data-stu-id="535ca-141">The interface has not implemented this method.</span></span><br/> |
| <dl> <span data-ttu-id="535ca-142"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-142"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="535ca-143">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="535ca-143">Out of memory.</span></span><br/>                                 |
| <dl> <span data-ttu-id="535ca-144"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="535ca-144"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="535ca-145">Um ponteiro inadequado foi passado para *ppFileList*.</span><span class="sxs-lookup"><span data-stu-id="535ca-145">A bad pointer was passed in for *ppFileList*.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="535ca-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="535ca-146">Remarks</span></span>

<span data-ttu-id="535ca-147">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="535ca-147">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="535ca-148">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="535ca-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="535ca-149">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="535ca-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="535ca-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="535ca-150">Requirements</span></span>



| <span data-ttu-id="535ca-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="535ca-151">Requirement</span></span> | <span data-ttu-id="535ca-152">Valor</span><span class="sxs-lookup"><span data-stu-id="535ca-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="535ca-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="535ca-153">Minimum supported client</span></span><br/> | <span data-ttu-id="535ca-154">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="535ca-154">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="535ca-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="535ca-155">Minimum supported server</span></span><br/> | <span data-ttu-id="535ca-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="535ca-156">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="535ca-157">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="535ca-157">End of client support</span></span><br/>    | <span data-ttu-id="535ca-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="535ca-158">Windows XP</span></span><br/>                                |
| <span data-ttu-id="535ca-159">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="535ca-159">End of server support</span></span><br/>    | <span data-ttu-id="535ca-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="535ca-160">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="535ca-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="535ca-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535ca-162">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="535ca-162">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
