---
title: palavra-chave sh_job
description: A \_ palavra-chave \ sh Job = especifica que o objeto do sistema é um identificador para um trabalho.
keywords:
- MIDL de palavra-chave sh_job
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103930053"
---
# <a name="sh_job-keyword"></a>\_palavra-chave sh Job

A palavra-chave **sh \_ Job** especifica que um `system_handle` contém um identificador para um trabalho.

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
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
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
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

[Objetos de trabalho](../procthread/job-objects.md)
</dt> <dt>

[Segurança do objeto de trabalho e direitos de acesso](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[Função **CreateJobObject**](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
