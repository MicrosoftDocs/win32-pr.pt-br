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
# <a name="shgetfolderpathex-function"></a>Função SHGetFolderPathEx

## <a name="description"></a>Description

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.
A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Recupera o caminho completo de uma pasta conhecida identificada pelo [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)da pasta.
Isso estende o [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) permitindo que você defina o tamanho inicial do buffer de cadeia de caracteres.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Parâmetros

### <a name="rfid-in"></a>RFID [in]

Uma referência ao **KNOWNFOLDERID** que identifica a pasta.

### <a name="dwflags-in"></a>dwFlags [in]

Sinalizadores que especificam opções de recuperação especiais.
Esse valor pode ser 0; caso contrário, um ou mais dos valores de [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .

### <a name="htoken-in-optional"></a>hToken [in, opcional]

Um [token de acesso](/windows/desktop/SecAuthZ/access-tokens) que representa um usuário específico.
Se esse parâmetro for **nulo**, que é o uso mais comum, a função solicitará a pasta conhecida para o usuário atual.

Solicite uma pasta de usuário específica, passando o *hToken* desse usuário.
Isso normalmente é feito no contexto de um serviço que tem privilégios suficientes para recuperar o token de um determinado usuário.
Esse token deve ser aberto com [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) e direitos de [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .
Em alguns casos, você também precisa incluir [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).
Além de passar o *hToken* do usuário, o hive do registro desse usuário específico deve ser montado.
Consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control) para obter mais informações sobre problemas de controle de acesso.

Atribuir o parâmetro *hToken* um valor de-1 indica o usuário padrão.
Isso permite que os clientes do [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) localizem locais de pasta (como a pasta de **área de trabalho** ) para o usuário padrão.
O perfil de usuário padrão é duplicado quando uma nova conta de usuário é criada e inclui pastas especiais, como **documentos** e **área de trabalho**.
Todos os itens adicionados à pasta de usuário padrão também aparecem em qualquer nova conta de usuário.
Observe que o acesso às pastas de usuário padrão requer privilégios de administrador.

### <a name="pszpath-out"></a>pszPath [saída]

Uma cadeia de caracteres Unicode terminada em nulo.
Esse buffer deve ter o tamanho cchPath.
Quando **SHGetFolderPathEx** retorna com êxito, esse parâmetro contém o caminho para a pasta conhecida.

### <a name="cchpath-in"></a>cchPath [in]

O tamanho do buffer *ppszPath* , em caracteres.

## <a name="returns"></a>Retornos

Retorna **S_OK** se obtiver êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Como [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) é um wrapper para [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), essa função (**SHGetFolderPathEx**) também serve como uma extensão para **SHGetFolderPath**.

## <a name="see-also"></a>Confira também

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[SHGetKnownFolderIDList](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
