---
title: palavra-chave sh_job
description: A palavra-chave \ sh \_ job\ especifica que o objeto do sistema é um identificador para um trabalho.
keywords:
- sh_job palavra-chave MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: dd71db0310b450db1d9c87879e8ac10ad998d1d21e48a60eb9d816c0a0718b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146279"
---
# <a name="sh_job-keyword"></a>\_Palavra-chave de trabalho sh

A **\_ palavra-chave de** trabalho sh especifica que um `system_handle` contém um alça para um trabalho.

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
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
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
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

[Objetos de trabalho](../procthread/job-objects.md)
</dt> <dt>

[Segurança e direitos de acesso do objeto de trabalho](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[**Função CreateJobObject**](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
