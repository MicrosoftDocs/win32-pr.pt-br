---
title: Mensagem de EM_GETHANDLE (WinUser. h)
description: Obtém um identificador da memória atualmente alocada para um texto do controle de edição de várias linhas.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- controles de Windows de mensagem de EM_GETHANDLE
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09ade5545197df2dbc9310b708cd7521334bba68f41a14329dd865e84fdee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019644"
---
# <a name="em_gethandle-message"></a>\_Mensagem em GEThandle

Obtém um identificador da memória atualmente alocada para um texto do controle de edição de várias linhas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um identificador de memória que identifica o buffer que contém o conteúdo do controle de edição. Se ocorrer um erro, como enviar a mensagem para um controle de edição de linha única, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Se a função for realizada com sucesso, o aplicativo poderá acessar o conteúdo do controle de edição, convertendo o valor de retorno para [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) e passando-o para [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** retorna um ponteiro para um buffer que é uma matriz terminada em nulo de **Char** s ou **WCHAR** s, dependendo se uma função ANSI ou Unicode criou o controle. Por exemplo, se [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) foi usado, o buffer é uma matriz de **Char** s, mas se **CreateWindowExW** foi usado, o buffer é uma matriz de **WCHAR** s. O aplicativo pode não alterar o conteúdo do buffer. Para desbloquear o buffer, o aplicativo chama [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) antes de permitir que o controle de edição receba novas mensagens.

> [!Note]  
> Para Comctl32.dll versão 6, o buffer sempre contém uma matriz de **WCHAR** s, independentemente de uma função ANSI ou Unicode ter criado o controle de edição. Para obter mais informações sobre versões de DLL, consulte [versões de controle comuns](common-control-versions.md).

 

Se seu aplicativo não puder obedecer às restrições impostas por em **\_ GetHandle**, use as funções [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) para copiar o conteúdo do controle de edição em um buffer fornecido pelo aplicativo.

**Edição avançada:** Não há suporte para a mensagem em **\_ GetHandle** . Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_ONhandle**](em-sethandle.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

