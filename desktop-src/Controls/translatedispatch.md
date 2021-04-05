---
title: Função de retorno de chamada TranslateDispatch
description: Usado pelo cliente da função doreadermode para interceptar e controlar explicitamente todas as mensagens do Windows direcionadas para a área de rolagem da janela do modo de leitura. Essa é uma função de retorno de chamada definida pelo aplicativo.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Controles do Windows da função de retorno de chamada TranslateDispatch
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918338"
---
# <a name="translatedispatch-callback-function"></a>Função de retorno de chamada TranslateDispatch

\[O *TranslateDispatch* está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Usado pelo cliente da função [**Doreadermode**](doreadermode.md) para interceptar e controlar explicitamente todas as mensagens do Windows direcionadas para a área de rolagem da janela do modo de leitura. Essa é uma função de retorno de chamada definida pelo aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpMsg* \[ no\]
</dt> <dd>

Tipo: **const [**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _

Um ponteiro para uma estrutura [_ *msg* *](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem interceptada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se a mensagem foi tratada por essa função; caso contrário, **false**. Se **for false**, a mensagem será tratada pela implementação do modo de leitor padrão. Essa implementação manipula movimentos e botões do mouse, bem como pressionamentos de tecla.

## <a name="examples"></a>Exemplos

O exemplo a seguir descreve uma implementação dessa função.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>          |



 

