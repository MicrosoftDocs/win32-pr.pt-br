---
description: Uma função de retorno de chamada definida pelo usuário que permite que o chamador da função CryptUIDlgSelectCertificate manipular a exibição de certificados que o usuário seleciona exibir.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Função de retorno de chamada PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978972"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Função de retorno de chamada PFNCCERTDISPLAYPROC

A **função PFNCCERTDISPLAYPROC** é uma função de retorno de chamada definida pelo usuário que permite que o chamador da função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) manipular a exibição de certificados que o usuário seleciona exibir.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCertContext* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura CONTEXT \_ CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa o certificado a ser exibido.

</dd> <dt>

*hWndSelCertDlg* \[ Em\]
</dt> <dd>

Um alça para a caixa de diálogo da qual o certificado foi selecionado para exibição.

</dd> <dt>

*pvCallbackData* \[ Em\]
</dt> <dd>

Dados adicionais usados pela função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna **TRUE** para indicar que trata a exibição do certificado e que a caixa de diálogo não deve exibir o certificado. Se essa função retornar **FALSE,** a caixa de diálogo exibirá o certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



 

 




