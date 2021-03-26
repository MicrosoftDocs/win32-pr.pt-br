---
UID: ''
title: Função SHGetFolderPathEx
description: Recupera o caminho de uma pasta conhecida identificada pelo KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104967156"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="f9906-103">Função SHGetFolderPathEx</span><span class="sxs-lookup"><span data-stu-id="f9906-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="f9906-104">Description</span><span class="sxs-lookup"><span data-stu-id="f9906-104">Description</span></span>

<span data-ttu-id="f9906-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="f9906-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="f9906-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="f9906-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f9906-107">Recupera o caminho completo de uma pasta conhecida identificada pelo [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)da pasta.</span><span class="sxs-lookup"><span data-stu-id="f9906-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="f9906-108">Isso estende o [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) permitindo que você defina o tamanho inicial do buffer de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9906-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="f9906-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9906-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="f9906-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="f9906-110">rfid [in]</span></span>

<span data-ttu-id="f9906-111">Uma referência ao **KNOWNFOLDERID** que identifica a pasta.</span><span class="sxs-lookup"><span data-stu-id="f9906-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="f9906-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="f9906-112">dwFlags [in]</span></span>

<span data-ttu-id="f9906-113">Sinalizadores que especificam opções de recuperação especiais.</span><span class="sxs-lookup"><span data-stu-id="f9906-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="f9906-114">Esse valor pode ser 0; caso contrário, um ou mais dos valores de [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .</span><span class="sxs-lookup"><span data-stu-id="f9906-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="f9906-115">hToken [in, opcional]</span><span class="sxs-lookup"><span data-stu-id="f9906-115">hToken [in, optional]</span></span>

<span data-ttu-id="f9906-116">Um [token de acesso](/windows/desktop/SecAuthZ/access-tokens) que representa um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="f9906-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="f9906-117">Se esse parâmetro for **nulo**, que é o uso mais comum, a função solicitará a pasta conhecida para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f9906-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="f9906-118">Solicite uma pasta de usuário específica, passando o *hToken* desse usuário.</span><span class="sxs-lookup"><span data-stu-id="f9906-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="f9906-119">Isso normalmente é feito no contexto de um serviço que tem privilégios suficientes para recuperar o token de um determinado usuário.</span><span class="sxs-lookup"><span data-stu-id="f9906-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="f9906-120">Esse token deve ser aberto com [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) e direitos de [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .</span><span class="sxs-lookup"><span data-stu-id="f9906-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="f9906-121">Em alguns casos, você também precisa incluir [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span><span class="sxs-lookup"><span data-stu-id="f9906-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="f9906-122">Além de passar o *hToken* do usuário, o hive do registro desse usuário específico deve ser montado.</span><span class="sxs-lookup"><span data-stu-id="f9906-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="f9906-123">Consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control) para obter mais informações sobre problemas de controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="f9906-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="f9906-124">Atribuir o parâmetro *hToken* um valor de-1 indica o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="f9906-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="f9906-125">Isso permite que os clientes do [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) localizem locais de pasta (como a pasta de **área de trabalho** ) para o usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="f9906-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="f9906-126">O perfil de usuário padrão é duplicado quando uma nova conta de usuário é criada e inclui pastas especiais, como **documentos** e **área de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="f9906-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="f9906-127">Todos os itens adicionados à pasta de usuário padrão também aparecem em qualquer nova conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="f9906-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="f9906-128">Observe que o acesso às pastas de usuário padrão requer privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="f9906-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="f9906-129">pszPath [saída]</span><span class="sxs-lookup"><span data-stu-id="f9906-129">pszPath [out]</span></span>

<span data-ttu-id="f9906-130">Uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="f9906-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="f9906-131">Esse buffer deve ter o tamanho cchPath.</span><span class="sxs-lookup"><span data-stu-id="f9906-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="f9906-132">Quando **SHGetFolderPathEx** retorna com êxito, esse parâmetro contém o caminho para a pasta conhecida.</span><span class="sxs-lookup"><span data-stu-id="f9906-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="f9906-133">cchPath [in]</span><span class="sxs-lookup"><span data-stu-id="f9906-133">cchPath [in]</span></span>

<span data-ttu-id="f9906-134">O tamanho do buffer *ppszPath* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="f9906-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="f9906-135">Retornos</span><span class="sxs-lookup"><span data-stu-id="f9906-135">Returns</span></span>

<span data-ttu-id="f9906-136">Retorna **S_OK** se obtiver êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f9906-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9906-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9906-137">Remarks</span></span>

<span data-ttu-id="f9906-138">Como [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) é um wrapper para [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), essa função (**SHGetFolderPathEx**) também serve como uma extensão para **SHGetFolderPath**.</span><span class="sxs-lookup"><span data-stu-id="f9906-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9906-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9906-139">See also</span></span>

[<span data-ttu-id="f9906-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="f9906-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="f9906-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="f9906-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="f9906-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="f9906-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="f9906-143">SHGetKnownFolderIDList</span><span class="sxs-lookup"><span data-stu-id="f9906-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="f9906-144">SHGetKnownFolderPath</span><span class="sxs-lookup"><span data-stu-id="f9906-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
