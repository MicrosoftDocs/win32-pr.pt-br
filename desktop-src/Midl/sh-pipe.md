---
title: palavra-chave sh_pipe
description: A \_ palavra-chave \ sh pipeName especifica que o objeto do sistema é um identificador para um pipe.
keywords:
- MIDL de palavra-chave sh_pipe
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "105814620"
---
# <a name="sh_pipe-keyword"></a>\_palavra-chave sh pipe

A palavra-chave **sh \_ pipe** especifica que um `system_handle` contém um identificador para um pipe.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Sobre pipes](../ipc/about-pipes.md)
</dt> <dt>

[Segurança de arquivo e direitos de acesso](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[Função **CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[Função **CreateNamedPipe**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
