---
title: Mensagem de LB_DIR (WinUser. h)
description: Adiciona nomes à lista exibida por uma caixa de listagem. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. \_O diretório lb também pode adicionar letras de unidade mapeadas à caixa de listagem.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- Controles de LB_DIR de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086329"
---
# <a name="lb_dir-message"></a><span data-ttu-id="1b87f-106">Mensagem de dir. LB \_</span><span class="sxs-lookup"><span data-stu-id="1b87f-106">LB\_DIR message</span></span>

<span data-ttu-id="1b87f-107">Adiciona nomes à lista exibida por uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="1b87f-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="1b87f-108">A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b87f-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="1b87f-109">**Lb \_ DIR** também pode adicionar letras de unidade mapeadas à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="1b87f-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b87f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b87f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b87f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b87f-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b87f-112">Os atributos dos arquivos ou diretórios a serem adicionados à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="1b87f-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="1b87f-113">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b87f-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="1b87f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1b87f-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="1b87f-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1b87f-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="1b87f-116"><dt>**\_arquivo DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="1b87f-117">Inclui arquivos arquivados.</span><span class="sxs-lookup"><span data-stu-id="1b87f-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="1b87f-118"><dt>**\_diretório DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="1b87f-119">Inclui subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="1b87f-119">Includes subdirectories.</span></span> <span data-ttu-id="1b87f-120">Os nomes de subdiretórios são colocados entre colchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="1b87f-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="1b87f-121"><dt>**\_unidades DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="1b87f-122">Todas as unidades mapeadas são adicionadas à lista.</span><span class="sxs-lookup"><span data-stu-id="1b87f-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="1b87f-123">As unidades são listadas no formato \[ - *x* - \] , em que *x* é a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="1b87f-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="1b87f-124"><dt>**exclusivo de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="1b87f-125">Inclui somente arquivos com os atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="1b87f-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="1b87f-126">Por padrão, os arquivos de leitura/gravação são listados mesmo que o DDL \_ ReadWrite não seja especificado.</span><span class="sxs-lookup"><span data-stu-id="1b87f-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="1b87f-127"><dt>**DDL \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="1b87f-128">Inclui arquivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="1b87f-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="1b87f-129"><dt>**\_somente leitura DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="1b87f-130">Inclui arquivos somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1b87f-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="1b87f-131"><dt>**ReadWrite de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="1b87f-132">Inclui arquivos de leitura/gravação sem atributos adicionais.</span><span class="sxs-lookup"><span data-stu-id="1b87f-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="1b87f-133">Essa é a configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="1b87f-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="1b87f-134"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="1b87f-135">Inclui arquivos do sistema.</span><span class="sxs-lookup"><span data-stu-id="1b87f-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="1b87f-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b87f-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b87f-137">Um ponteiro para a cadeia de caracteres terminada em nulo que especifica um caminho absoluto, um caminho relativo ou um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1b87f-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="1b87f-138">Um caminho absoluto pode começar com uma letra da unidade (por exemplo, d: \) ou um nome UNC (por exemplo, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="1b87f-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="1b87f-139">Se a cadeia de caracteres especificar um nome de arquivo ou diretório que tenha os atributos especificados pelo parâmetro *wParam* , o nome do arquivo ou diretório será adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="1b87f-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="1b87f-140">Se o nome de arquivo ou diretório contiver caracteres curinga (?</span><span class="sxs-lookup"><span data-stu-id="1b87f-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="1b87f-141">ou \* ), todos os arquivos ou diretórios que correspondem à expressão curinga e têm os atributos especificados pelo parâmetro *wParam* são adicionados à lista.</span><span class="sxs-lookup"><span data-stu-id="1b87f-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b87f-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b87f-142">Return value</span></span>

<span data-ttu-id="1b87f-143">Se a mensagem tiver sucesso, o valor de retorno será o índice de base zero do sobrenome adicionado à lista.</span><span class="sxs-lookup"><span data-stu-id="1b87f-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="1b87f-144">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="1b87f-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="1b87f-145">Se não houver espaço suficiente para armazenar as novas cadeias de caracteres, o valor de retorno será LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="1b87f-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b87f-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b87f-146">Remarks</span></span>

<span data-ttu-id="1b87f-147">A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="1b87f-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="1b87f-148">Ele reserva a quantidade especificada de memória para que as mensagens de **\_ dir de lb** subsequentes tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="1b87f-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="1b87f-149">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="1b87f-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="1b87f-150">Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="1b87f-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="1b87f-151">Se *wParam* incluir o \_ sinalizador de diretório DDL e *lParam* especificar todos os subdiretórios de um diretório de primeiro nível, como C: \\ temp \\ \* , a caixa de listagem sempre incluirá uma entrada ".." para o diretório raiz.</span><span class="sxs-lookup"><span data-stu-id="1b87f-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="1b87f-152">Isso é verdadeiro mesmo que o diretório raiz tenha atributos ocultos ou de sistema e os \_ sinalizadores de sistema ocultos e DDL DDL \_ não sejam especificados.</span><span class="sxs-lookup"><span data-stu-id="1b87f-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="1b87f-153">O diretório raiz de um volume NTFS tem atributos ocultos e de sistema.</span><span class="sxs-lookup"><span data-stu-id="1b87f-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="1b87f-154">A lista exibe nomes de FileName longos, se houver.</span><span class="sxs-lookup"><span data-stu-id="1b87f-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="1b87f-155">Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="1b87f-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="1b87f-156">Isso pode causar problemas.</span><span class="sxs-lookup"><span data-stu-id="1b87f-156">This can cause problems.</span></span> <span data-ttu-id="1b87f-157">Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows em Japonês ficarão confusos.</span><span class="sxs-lookup"><span data-stu-id="1b87f-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="1b87f-158">Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="1b87f-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b87f-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b87f-159">Requirements</span></span>



| <span data-ttu-id="1b87f-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b87f-160">Requirement</span></span> | <span data-ttu-id="1b87f-161">Valor</span><span class="sxs-lookup"><span data-stu-id="1b87f-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b87f-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b87f-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1b87f-163">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b87f-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b87f-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b87f-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1b87f-165">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b87f-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b87f-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b87f-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b87f-167"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b87f-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b87f-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b87f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b87f-169">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="1b87f-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





