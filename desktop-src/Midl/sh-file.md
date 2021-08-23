---
title: palavra-chave sh_file
description: A \_ palavra-chave \ sh file\ especifica que o objeto do sistema é um identificador para um arquivo.
keywords:
- sh_file palavra-chave MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 05b76ad772ca628a28677d9b0da06252d0fec70251a4a197d39b50b9760ef931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013624"
---
# <a name="sh_file-keyword"></a>\_Palavra-chave de arquivo sh

A **\_ palavra-chave de** arquivo sh especifica que um `system_handle` contém um handle para um arquivo.

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a>Parâmetros

Essa palavra-chave é um parâmetro [**para system_handle**](system-handle.md).

A [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do *parâmetro access-rights.* O comportamento padrão é `DUPLICATE_SAME_ACCESS` de acordo com as [especificações de função **DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Comentários

Para usar essa palavra-chave com o `system_handle` atributo , o sinalizador deve ser definido como `-target` `NT100` (ou superior) ao executar midl.exe.

## <a name="examples"></a>Exemplos

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo com suporte | Windows 10 Atualização de aniversário (versão 1607, build 14393) |
| Servidor mínimo com suporte | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Segurança de arquivos e direitos de acesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**Função DCompositionCreateSurfaceHandle**](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
