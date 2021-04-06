---
description: Uma função de retorno de chamada definida pelo usuário que permite que o chamador da função CryptUIDlgSelectCertificate manipule a exibição de certificados que o usuário seleciona para exibir.
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
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011079"
---
# <a name="pfnccertdisplayproc-callback-function"></a>Função de retorno de chamada PFNCCERTDISPLAYPROC

A função **PFNCCERTDISPLAYPROC** é uma função de retorno de chamada definida pelo usuário que permite que o chamador da função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) manipule a exibição de certificados que o usuário seleciona para exibir.

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

*pCertContext* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa o certificado a ser exibido.

</dd> <dt>

*hWndSelCertDlg* \[ no\]
</dt> <dd>

Um identificador para a caixa de diálogo da qual o certificado foi selecionado para exibição.

</dd> <dt>

*pvCallbackData* \[ no\]
</dt> <dd>

Dados adicionais usados pela função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna **true** para indicar que ele lida com a exibição do certificado e que a caixa de diálogo não deve exibir o certificado. Se essa função retornar **false**, a caixa de diálogo exibirá o certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



 

 




