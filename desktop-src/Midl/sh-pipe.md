---
title: palavra-chave sh_pipe
description: A \_ palavra-chave \ sh pipe\ especifica que o objeto do sistema é um identificador para um pipe.
keywords:
- sh_pipe palavra-chave MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 15bee0e34525d83af10e5c42199116dc6080a6a7b7f4e2af3de565f62a9c6a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383341"
---
# <a name="sh_pipe-keyword"></a>\_Palavra-chave sh pipe

A **\_ palavra-chave sh pipe** especifica que um mantém um alça para um `system_handle` pipe.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Sobre pipes](../ipc/about-pipes.md)
</dt> <dt>

[Segurança de arquivos e direitos de acesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**Função CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**Função CreateNamedPipe**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
