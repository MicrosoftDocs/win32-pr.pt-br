---
title: palavra-chave sh_event
description: A \_ palavra-chave \ sh Event \ especifica que o objeto do sistema é um identificador para um evento.
keywords:
- MIDL de palavra-chave sh_event
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b2f489c27d32c40f80cef326b99131158df92cad2183cee1dc5a3dd74310cf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013644"
---
# <a name="sh_event-keyword"></a>\_palavra-chave do evento sh

A palavra-chave do **\_ evento sh** especifica que um `system_handle` contém um identificador para um evento.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo com suporte | Windows 10 Atualização de aniversário (versão 1607, Build 14393) |
| Servidor mínimo com suporte | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Objetos de evento](../sync/event-objects.md)
</dt> <dt>

[Segurança do objeto de sincronização e direitos de acesso](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Função **CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[Função **CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
