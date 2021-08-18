---
title: palavra-chave sh_token
description: A \_ palavra-chave \ sh token \ especifica que o objeto do sistema é um identificador para um token.
keywords:
- MIDL de palavra-chave sh_token
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8305a8073d03eb90bbd214f1b56cb1174ffef66953bb170fb7f28ebf1b84d35c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066767"
---
# <a name="sh_token-keyword"></a>\_palavra-chave sh token

A palavra-chave **sh \_ token** especifica que um `system_handle` contém um identificador para um token.

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
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
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
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

[Tokens de acesso](../secauthz/access-tokens.md)
</dt> <dt>

[Direitos de acesso para objetos de Access-Token](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
