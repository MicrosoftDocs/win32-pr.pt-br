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
# <a name="istorageprovidercopyhookcopycallback-method"></a>Método IStorageProviderCopyHook:: CopyCallback

Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.

## <a name="syntax"></a>Sintaxe

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

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela que o manipulador de cabo de cópia deve usar como pai para qualquer elemento de interface do usuário que o manipulador possa precisar exibir. Se **FOF_SILENT** for especificado em *operação*, o método deverá ignorar esse parâmetro.

</dd> </dl>

<dl> <dt>

*operação* \[ do no\]
</dt> <dd>

A operação a ser executada. Esse parâmetro pode ser um dos valores listados no membro **wFunc** da estrutura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .

</dd> </dl>

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Os sinalizadores que controlam a operação. Esse parâmetro pode ser um ou mais dos valores listados no membro *fFlags* da estrutura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .

Para ganchos de cópia de impressora, esse valor é um dos seguintes valores definidos em shellapi. h.

| Valor       | Descrição |
|-------------|------------|
|  **PO_DELETE**      | Uma impressora está sendo excluída. O parâmetro *srcFile* aponta para o caminho completo para a impressora especificada.           |
|  **PO_RENAME**       | Uma impressora está sendo renomeada. O parâmetro *srcFile* aponta para o novo nome da impressora. O parâmetro *destfile* aponta para o nome antigo.           |
| **PO_PORTCHANGE**    | Não há suporte. Não use.          |
| **PO_REN_PORT**    | Não há suporte. Não use.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome da pasta de origem.

</dd> </dl>

*srcAttribs* \[ no\]
</dt> <dd>

Os atributos da pasta de origem. Esse parâmetro pode ser uma combinação de qualquer um dos sinalizadores de atributo de arquivo (FILE_ATTRIBUTE_ *) definidos nos arquivos de cabeçalho. Consulte [constantes de atributo de arquivo](../fileio/file-attribute-constants.md).

</dd> </dl>

*destfile* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome da pasta de destino.

</dd> </dl>

*destAttribs* \[ no\]
</dt> <dd>

Os atributos da pasta de destino. Esse parâmetro pode ser uma combinação de qualquer um dos sinalizadores de atributo de arquivo (FILE_ATTRIBUTE_ *) definidos nos arquivos de cabeçalho. Consulte [constantes de atributo de arquivo](../fileio/file-attribute-constants.md).

</dd> </dl>

*resultado* \[ fora\]
</dt> <dd>

O valor inteiro que indica se o Shell deve executar a operação. Um dos seguintes:

| Valor       | Descrição |
|-------------|------------|
| **IDYES**       | Permite a operação.           |
| **IDNO**        | Impede a operação nessa pasta, mas continua com outras operações que foram aprovadas (por exemplo, uma operação de cópia em lote).           |
| **IDCANCEL**    | Impede a operação atual e cancela as operações pendentes.           |


</dd> </dl>


## <a name="return-value"></a>Retornar valor

Retorna **S_OK** se for bem-sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

O Shell chama o manipulador de conexão de cópia do provedor de nuvem para cada pasta na raiz de sincronização registrada. Para registrar um manipulador de gancho de cópia para pastas de nuvem, defina o valor **CopyHook** sob a chave **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CURRENTVERSION/Explorer/SYNCROOTMANAGER/{SYNCROOTID}** para o CLSID do objeto de cabo de cópia.

Quando o método **CopyCallback** é chamado, o Shell Inicializa a interface [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) diretamente sem usar uma interface [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) primeiro.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Build 19624 do Windows 10 Insider Preview                                |
| parâmetro                   | ShObjIdl. h   |

## <a name="see-also"></a>Confira também

[Criar um mecanismo de sincronização de nuvem que dê suporte a arquivos de espaço reservado](../cfapi/build-a-cloud-file-sync-engine.md)