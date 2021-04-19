---
title: palavra-chave sh_process
description: A \_ palavra-chave \ sh Process \ especifica que o objeto do sistema é um identificador para um processo.
keywords:
- MIDL de palavra-chave sh_process
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105793781"
---
# <a name="sh_process-keyword"></a>\_palavra-chave sh Process

A palavra-chave **sh \_ process** especifica que um `system_handle` tem um identificador para um processo.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a>Parâmetros

Essa palavra-chave é um parâmetro para [**system_handle**](system-handle.md).

A documentação [**system_handle**](system-handle.md) também contém detalhes sobre o uso opcional do parâmetro *Access-Rights* . O comportamento padrão é de acordo com as `DUPLICATE_SAME_ACCESS` especificações de [função **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Comentários

Para usar essa palavra-chave com o `system_handle` atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) durante a execução de midl.exe.

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
| Cliente mínimo com suporte | Atualização de aniversário do Windows 10 (versão 1607, Build 14393) |
| Servidor mínimo com suporte | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Sobre Processos e Threads](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Direitos de acesso e segurança do processo](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[Função **CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[Função **OpenProcess**](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>