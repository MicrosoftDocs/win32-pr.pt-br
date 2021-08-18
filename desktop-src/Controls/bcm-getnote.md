---
title: Mensagem de BCM_GETNOTE (commctrl. h)
description: Obtém o texto da nota associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a macro do botão \_ getnote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- controles de Windows de mensagem de BCM_GETNOTE
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b552f79e1d6c7bda2808b99701ff11e45deb169232b8bb52c4ecf231cdcbfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921696"
---
# <a name="bcm_getnote-message"></a>\_Mensagem de GETnote do BCM

Obtém o texto da nota associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a macro do [**botão \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ entrada, saída\]
</dt> <dd>

Um **DWORD** que especifica o tamanho do buffer apontado por *lParam*, em caracteres.

</dd> <dt>

*lParam* \[ fora\]
</dt> <dd>

O buffer de cadeia de caracteres para receber o texto. O buffer deve ser grande o suficiente para acomodar o caractere nulo de terminação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

A mensagem do **BCM \_ getnote** funciona apenas com botões que têm o estilo de botão [**BS \_ COMMANDLINK**](button-styles.md) ou [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) conterá:

-   \_Não \_ há suporte para o erro, se o botão não tiver o estilo [**BS \_ DEFCOMMANDLINK**](button-styles.md) ou [**BS \_ COMMANDLINK**](button-styles.md) .
-   ERRO \_ \_ de buffer insuficiente se o buffer de *lParam* for muito pequeno. O parâmetro *wParam* conterá o tamanho de buffer necessário, em caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Tipos de botão](button-types-and-styles.md)
</dt> </dl>

 

