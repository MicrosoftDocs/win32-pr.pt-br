---
title: palavra-chave sh_socket
description: A palavra-chave \ sh \_ socket\ especifica que o objeto do sistema é um identificador para um soquete.
keywords:
- sh_socket palavra-chave MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 542610d586af084f4238e70cd0e6c848099e4d2153d0feab8d617475a50476e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822096"
---
# <a name="sh_socket-keyword"></a>\_Palavra-chave sh socket

A **\_ palavra-chave sh socket** especifica que um `system_handle` contém um alça para um soquete.

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
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
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
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

[Windows Soquetes 2](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
