---
title: Mensagem de CB_DIR (WinUser. h)
description: Adiciona nomes à lista exibida pela caixa de combinação. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. \_O diretório CB também pode adicionar letras de unidade mapeadas à lista.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Controles de CB_DIR de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824410"
---
# <a name="cb_dir-message"></a><span data-ttu-id="e25e2-106">\_Mensagem de diretório CB</span><span class="sxs-lookup"><span data-stu-id="e25e2-106">CB\_DIR message</span></span>

<span data-ttu-id="e25e2-107">Adiciona nomes à lista exibida pela caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e25e2-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="e25e2-108">A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e25e2-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="e25e2-109">**CB \_ DIR** também pode adicionar letras de unidade mapeadas à lista.</span><span class="sxs-lookup"><span data-stu-id="e25e2-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="e25e2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e25e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e25e2-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e25e2-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e25e2-112">Os atributos dos arquivos ou diretórios a serem adicionados à caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e25e2-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="e25e2-113">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e25e2-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e25e2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e25e2-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="e25e2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="e25e2-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="e25e2-116"><dt>**\_arquivo DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="e25e2-117">Inclui arquivos arquivados.</span><span class="sxs-lookup"><span data-stu-id="e25e2-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="e25e2-118"><dt>**\_diretório DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="e25e2-119">Inclui subdiretórios, que são colocados entre colchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="e25e2-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="e25e2-120"><dt>**\_unidades DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="e25e2-121">Todas as unidades mapeadas são adicionadas à lista.</span><span class="sxs-lookup"><span data-stu-id="e25e2-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="e25e2-122">As unidades são listadas no formato \[ - *x* - \] , em que *x* é a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="e25e2-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="e25e2-123"><dt>**exclusivo de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="e25e2-124">Inclui somente arquivos com os atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="e25e2-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="e25e2-125">Por padrão, os arquivos de leitura/gravação são listados mesmo que o DDL \_ ReadWrite não seja especificado.</span><span class="sxs-lookup"><span data-stu-id="e25e2-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="e25e2-126"><dt>**DDL \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="e25e2-127">Inclui arquivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="e25e2-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="e25e2-128"><dt>**\_somente leitura DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="e25e2-129">Inclui arquivos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e25e2-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="e25e2-130"><dt>**ReadWrite de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="e25e2-131">Inclui arquivos de leitura/gravação sem atributos adicionais.</span><span class="sxs-lookup"><span data-stu-id="e25e2-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="e25e2-132">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="e25e2-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="e25e2-133"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="e25e2-134">Inclui arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e25e2-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="e25e2-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e25e2-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e25e2-136">Um ponteiro **LPCTSTR** para uma cadeia de caracteres terminada em nulo que especifica um caminho absoluto, um caminho relativo ou um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e25e2-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="e25e2-137">Um caminho absoluto pode começar com uma letra da unidade (por exemplo, d: \) ou um nome UNC (por exemplo, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="e25e2-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="e25e2-138">Se a cadeia de caracteres especificar um nome de arquivo ou diretório que tenha os atributos especificados pelo parâmetro *wParam* , o nome do arquivo ou diretório será adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="e25e2-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="e25e2-139">Se o nome do arquivo ou o nome do diretório contiver caracteres curinga (?</span><span class="sxs-lookup"><span data-stu-id="e25e2-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="e25e2-140">ou \* ), todos os arquivos ou diretórios que correspondem à expressão curinga e têm os atributos especificados pelo parâmetro *wParam* são adicionados à lista exibida na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e25e2-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e25e2-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e25e2-141">Return value</span></span>

<span data-ttu-id="e25e2-142">Se a mensagem tiver sucesso, o valor de retorno será o índice de base zero do sobrenome adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="e25e2-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="e25e2-143">Se ocorrer um erro, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="e25e2-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="e25e2-144">Se não houver espaço suficiente para armazenar as novas cadeias de caracteres, o valor de retorno será CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="e25e2-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e25e2-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="e25e2-145">Remarks</span></span>

<span data-ttu-id="e25e2-146">Se *wParam* incluir o \_ sinalizador de diretório DDL e *lParam* especificar todos os subdiretórios de um diretório de primeiro nível, como C: \\ temp \\ \* , a caixa de listagem sempre incluirá uma entrada ".." para o diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="e25e2-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="e25e2-147">Isso é verdadeiro mesmo que o diretório raiz tenha atributos ocultos ou de sistema e os \_ sinalizadores de sistema ocultos e DDL DDL \_ não sejam especificados.</span><span class="sxs-lookup"><span data-stu-id="e25e2-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="e25e2-148">O diretório raiz de um volume NTFS tem atributos ocultos e de sistema.</span><span class="sxs-lookup"><span data-stu-id="e25e2-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="e25e2-149">A lista exibe nomes de arquivo longos, se houver.</span><span class="sxs-lookup"><span data-stu-id="e25e2-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="e25e2-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e25e2-150">Requirements</span></span>



| <span data-ttu-id="e25e2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="e25e2-151">Requirement</span></span> | <span data-ttu-id="e25e2-152">Valor</span><span class="sxs-lookup"><span data-stu-id="e25e2-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e25e2-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e25e2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e25e2-154">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e25e2-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e25e2-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e25e2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e25e2-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e25e2-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e25e2-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e25e2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e25e2-158"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e25e2-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e25e2-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="e25e2-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="e25e2-160">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e25e2-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e25e2-161">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="e25e2-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="e25e2-162">**inserção de CB \_**</span><span class="sxs-lookup"><span data-stu-id="e25e2-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="e25e2-163">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="e25e2-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





