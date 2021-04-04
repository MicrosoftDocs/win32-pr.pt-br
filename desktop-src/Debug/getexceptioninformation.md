---
description: Recupera uma descrição independente de computador de uma exceção e informações sobre o estado do computador que existe para o thread quando a exceção ocorre. Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: Macro GetExceptionInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646497"
---
# <a name="getexceptioninformation-macro"></a>Macro GetExceptionInformation

Recupera uma descrição independente de computador de uma exceção e informações sobre o estado do computador que existe para o thread quando a exceção ocorre. Essa função pode ser chamada somente de dentro da expressão de filtro de um manipulador de exceção.

> [!Note]  
> O compilador de otimização do Microsoft C/C++ interpreta essa função como uma palavra-chave e seu uso fora da sintaxe apropriada de tratamento de exceção gera um erro de compilador.

 

## <a name="syntax"></a>Sintaxe


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parâmetros

Esta macro não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Um ponteiro para uma [**exceção \_ aponta**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para uma estrutura que contém ponteiros para as duas estruturas a seguir:

-   [**Exceção \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Estrutura de registro que contém uma descrição da exceção.
-   Estrutura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contém as informações de estado do computador.

## <a name="remarks"></a>Comentários

A expressão de filtro (da qual a função é chamada) é avaliada se ocorre uma exceção durante a execução do bloco **\_ \_ try** e determina se o bloco **\_ \_ Except** será ou não executado.

A expressão de filtro pode invocar uma função de filtro. A função Filter não pode chamar **GetExceptionInformation**. No entanto, o valor de retorno de **GetExceptionInformation** pode ser passado como um parâmetro para uma função de filtro.

Para passar as informações de [**\_ ponteiros de exceção**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) para o bloco de manipulador de exceção, a expressão de filtro ou a função de filtro deve copiar o ponteiro ou os dados para o armazenamento seguro que o manipulador pode acessar posteriormente.

No caso de manipuladores aninhados, cada expressão de filtro é avaliada até que uma seja avaliada como **exceção \_ executar \_ manipulador** ou **exceção \_ continuar \_ execução**. Cada expressão de filtro pode invocar **GetExceptionInformation** para obter informações de exceção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NOTICIOSO**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**\_ponteiros de exceção**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**registro de exceção \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funções de manipulação de exceção estruturada](structured-exception-handling-functions.md)
</dt> <dt>

[Visão geral da manipulação de exceção estruturada](structured-exception-handling.md)
</dt> <dt>

[Habilitar o suporte do Windows para Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
