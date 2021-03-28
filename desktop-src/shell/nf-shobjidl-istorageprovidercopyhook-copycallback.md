---
description: Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104989122"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a><span data-ttu-id="7332e-103">Método IStorageProviderCopyHook:: CopyCallback</span><span class="sxs-lookup"><span data-stu-id="7332e-103">IStorageProviderCopyHook::CopyCallback method</span></span>

<span data-ttu-id="7332e-104">Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.</span><span class="sxs-lookup"><span data-stu-id="7332e-104">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="syntax"></a><span data-ttu-id="7332e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7332e-105">Syntax</span></span>

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a><span data-ttu-id="7332e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7332e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7332e-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-107">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-108">Um identificador para a janela que o manipulador de cabo de cópia deve usar como pai para qualquer elemento de interface do usuário que o manipulador possa precisar exibir.</span><span class="sxs-lookup"><span data-stu-id="7332e-108">A handle to the window that the copy hook handler should use as the parent for any user interface elements the handler may need to display.</span></span> <span data-ttu-id="7332e-109">Se **FOF_SILENT** for especificado em *operação*, o método deverá ignorar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7332e-109">If **FOF_SILENT** is specified in *operation*, the method should ignore this parameter.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7332e-110">*operação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-110">*operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-111">A operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="7332e-111">The operation to perform.</span></span> <span data-ttu-id="7332e-112">Esse parâmetro pode ser um dos valores listados no membro **wFunc** da estrutura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="7332e-112">This parameter can be one of the values listed under the **wFunc** member of the [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7332e-113">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-114">Os sinalizadores que controlam a operação.</span><span class="sxs-lookup"><span data-stu-id="7332e-114">The flags that control the operation.</span></span> <span data-ttu-id="7332e-115">Esse parâmetro pode ser um ou mais dos valores listados no membro *fFlags* da estrutura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="7332e-115">This parameter can be one or more of the values listed under the *fFlags* member of the [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) structure.</span></span>

<span data-ttu-id="7332e-116">Para ganchos de cópia de impressora, esse valor é um dos seguintes valores definidos em shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="7332e-116">For printer copy hooks, this value is one of the following values defined in shellapi.h.</span></span>

| <span data-ttu-id="7332e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7332e-117">Value</span></span>       | <span data-ttu-id="7332e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7332e-118">Description</span></span> |
|-------------|------------|
|  <span data-ttu-id="7332e-119">**PO_DELETE**</span><span class="sxs-lookup"><span data-stu-id="7332e-119">**PO_DELETE**</span></span>      | <span data-ttu-id="7332e-120">Uma impressora está sendo excluída.</span><span class="sxs-lookup"><span data-stu-id="7332e-120">A printer is being deleted.</span></span> <span data-ttu-id="7332e-121">O parâmetro *srcFile* aponta para o caminho completo para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="7332e-121">The *srcFile* parameter points to the full path to the specified printer.</span></span>           |
|  <span data-ttu-id="7332e-122">**PO_RENAME**</span><span class="sxs-lookup"><span data-stu-id="7332e-122">**PO_RENAME**</span></span>       | <span data-ttu-id="7332e-123">Uma impressora está sendo renomeada.</span><span class="sxs-lookup"><span data-stu-id="7332e-123">A printer is being renamed.</span></span> <span data-ttu-id="7332e-124">O parâmetro *srcFile* aponta para o novo nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="7332e-124">The *srcFile* parameter points to the printer's new name.</span></span> <span data-ttu-id="7332e-125">O parâmetro *destfile* aponta para o nome antigo.</span><span class="sxs-lookup"><span data-stu-id="7332e-125">The *destFile* parameter points to the old name.</span></span>           |
| <span data-ttu-id="7332e-126">**PO_PORTCHANGE**</span><span class="sxs-lookup"><span data-stu-id="7332e-126">**PO_PORTCHANGE**</span></span>    | <span data-ttu-id="7332e-127">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7332e-127">Not supported.</span></span> <span data-ttu-id="7332e-128">Não use.</span><span class="sxs-lookup"><span data-stu-id="7332e-128">Do not use.</span></span>          |
| <span data-ttu-id="7332e-129">**PO_REN_PORT**</span><span class="sxs-lookup"><span data-stu-id="7332e-129">**PO_REN_PORT**</span></span>    | <span data-ttu-id="7332e-130">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="7332e-130">Not supported.</span></span> <span data-ttu-id="7332e-131">Não use.</span><span class="sxs-lookup"><span data-stu-id="7332e-131">Do not use.</span></span>           |

</dd> </dl>

<dl> <dt>

<span data-ttu-id="7332e-132">*srcFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-132">*srcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-133">Um ponteiro para uma cadeia de caracteres que contém o nome da pasta de origem.</span><span class="sxs-lookup"><span data-stu-id="7332e-133">A pointer to a string that contains the name of the source folder.</span></span>

</dd> </dl>

<span data-ttu-id="7332e-134">*srcAttribs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-134">*srcAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-135">Os atributos da pasta de origem.</span><span class="sxs-lookup"><span data-stu-id="7332e-135">The attributes of the source folder.</span></span> <span data-ttu-id="7332e-136">Esse parâmetro pode ser uma combinação de qualquer um dos sinalizadores de atributo de arquivo (FILE_ATTRIBUTE_ \*) definidos nos arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="7332e-136">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="7332e-137">Consulte [constantes de atributo de arquivo](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7332e-137">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="7332e-138">*destfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-138">*destFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-139">Um ponteiro para uma cadeia de caracteres que contém o nome da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="7332e-139">A pointer to a string that contains the name of the destination folder.</span></span>

</dd> </dl>

<span data-ttu-id="7332e-140">*destAttribs* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7332e-140">*destAttribs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-141">Os atributos da pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="7332e-141">The attributes of the destination folder.</span></span> <span data-ttu-id="7332e-142">Esse parâmetro pode ser uma combinação de qualquer um dos sinalizadores de atributo de arquivo (FILE_ATTRIBUTE_ \*) definidos nos arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="7332e-142">This parameter can be a combination of any of the file attribute flags (FILE_ATTRIBUTE_\*) defined in the header files.</span></span> <span data-ttu-id="7332e-143">Consulte [constantes de atributo de arquivo](../fileio/file-attribute-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7332e-143">See [File Attribute Constants](../fileio/file-attribute-constants.md).</span></span>

</dd> </dl>

<span data-ttu-id="7332e-144">*resultado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7332e-144">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7332e-145">O valor inteiro que indica se o Shell deve executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7332e-145">The integer value that indicates whether the Shell should perform the operation.</span></span> <span data-ttu-id="7332e-146">Um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7332e-146">One of the following:</span></span>

| <span data-ttu-id="7332e-147">Valor</span><span class="sxs-lookup"><span data-stu-id="7332e-147">Value</span></span>       | <span data-ttu-id="7332e-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="7332e-148">Description</span></span> |
|-------------|------------|
| <span data-ttu-id="7332e-149">**IDYES**</span><span class="sxs-lookup"><span data-stu-id="7332e-149">**IDYES**</span></span>       | <span data-ttu-id="7332e-150">Permite a operação.</span><span class="sxs-lookup"><span data-stu-id="7332e-150">Allows the operation.</span></span>           |
| <span data-ttu-id="7332e-151">**IDNO**</span><span class="sxs-lookup"><span data-stu-id="7332e-151">**IDNO**</span></span>        | <span data-ttu-id="7332e-152">Impede a operação nessa pasta, mas continua com outras operações que foram aprovadas (por exemplo, uma operação de cópia em lote).</span><span class="sxs-lookup"><span data-stu-id="7332e-152">Prevents the operation on this folder but continues with any other operations that have been approved (for example, a batch copy operation).</span></span>           |
| <span data-ttu-id="7332e-153">**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="7332e-153">**IDCANCEL**</span></span>    | <span data-ttu-id="7332e-154">Impede a operação atual e cancela as operações pendentes.</span><span class="sxs-lookup"><span data-stu-id="7332e-154">Prevents the current operation and cancels any pending operations.</span></span>           |


</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="7332e-155">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7332e-155">Return value</span></span>

<span data-ttu-id="7332e-156">Retorna **S_OK** se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="7332e-156">Returns **S_OK** if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7332e-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="7332e-157">Remarks</span></span>

<span data-ttu-id="7332e-158">O Shell chama o manipulador de conexão de cópia do provedor de nuvem para cada pasta na raiz de sincronização registrada.</span><span class="sxs-lookup"><span data-stu-id="7332e-158">The Shell calls the cloud provider's copy hook handler for every folder under the registered sync root.</span></span> <span data-ttu-id="7332e-159">Para registrar um manipulador de gancho de cópia para pastas de nuvem, defina o valor **CopyHook** sob a chave **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CURRENTVERSION/Explorer/SYNCROOTMANAGER/{SYNCROOTID}** para o CLSID do objeto de cabo de cópia.</span><span class="sxs-lookup"><span data-stu-id="7332e-159">To register a copy hook handler for cloud folders, set the **CopyHook** value under the **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** key to the CLSID of the copy hook object.</span></span>

<span data-ttu-id="7332e-160">Quando o método **CopyCallback** é chamado, o Shell Inicializa a interface [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) diretamente sem usar uma interface [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) primeiro.</span><span class="sxs-lookup"><span data-stu-id="7332e-160">When the **CopyCallback** method is called, the Shell initializes the [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) interface directly without using an [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface first.</span></span>

## <a name="requirements"></a><span data-ttu-id="7332e-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7332e-161">Requirements</span></span>

| <span data-ttu-id="7332e-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="7332e-162">Requirement</span></span> | <span data-ttu-id="7332e-163">Valor</span><span class="sxs-lookup"><span data-stu-id="7332e-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7332e-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7332e-164">Minimum supported client</span></span> | <span data-ttu-id="7332e-165">Build 19624 do Windows 10 Insider Preview</span><span class="sxs-lookup"><span data-stu-id="7332e-165">Windows 10 Insider Preview Build 19624</span></span>                                |
| <span data-ttu-id="7332e-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7332e-166">Header</span></span>                   | <span data-ttu-id="7332e-167">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="7332e-167">shobjidl.h</span></span>   |

## <a name="see-also"></a><span data-ttu-id="7332e-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="7332e-168">See also</span></span>

[<span data-ttu-id="7332e-169">Criar um mecanismo de sincronização de nuvem que dê suporte a arquivos de espaço reservado</span><span class="sxs-lookup"><span data-stu-id="7332e-169">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](../cfapi/build-a-cloud-file-sync-engine.md)