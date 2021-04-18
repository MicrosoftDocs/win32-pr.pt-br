---
title: palavra-chave sh_mutex
description: A \_ palavra-chave \ sh mutex \ especifica que o objeto do sistema é um identificador para um mutex.
keywords:
- MIDL de palavra-chave sh_mutex
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105795517"
---
# <a name="sh_mutex-keyword"></a>\_palavra-chave sh mutex

A palavra-chave **sh \_ mutex** especifica que um `system_handle` mantém um identificador para um mutex.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
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
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
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

[Objetos mutex](../sync/mutex-objects.md)
</dt> <dt>

[Segurança do objeto de sincronização e direitos de acesso](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Função **CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[Função **CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>