---
title: palavra-chave sh_reg_key
description: A palavra-chave \ sh \_ reg \_ Key \ especifica que o objeto do sistema é um identificador para uma chave do registro.
keywords:
- MIDL de palavra-chave sh_reg_key
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105766009"
---
# <a name="sh_reg_key-keyword"></a>\_palavra-chave da chave de registro sh \_

A palavra-chave **sh \_ reg \_ Key** especifica que um `system_handle` mantém um identificador para uma chave do registro.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
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
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registro](../sysinfo/registry.md)
</dt> <dt>

[Segurança da chave do registro e direitos de acesso](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[Função **RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
