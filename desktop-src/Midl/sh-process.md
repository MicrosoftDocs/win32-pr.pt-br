---
title: palavra-chave sh_process
description: A palavra-chave \ sh \_ process\ especifica que o objeto do sistema é um identificador para um processo.
keywords:
- sh_process palavra-chave MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3dc11f2980e5124bbc76d0b57fce21d8007b0c09905ca47707d5be6fbb112d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146269"
---
# <a name="sh_process-keyword"></a>\_Palavra-chave de processo sh

A **\_ palavra-chave de** processo sh especifica que um `system_handle` contém um handle para um processo.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
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
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
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

[Sobre Processos e Threads](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Processar direitos de acesso e segurança](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[**Função CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**Função OpenProcess**](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>