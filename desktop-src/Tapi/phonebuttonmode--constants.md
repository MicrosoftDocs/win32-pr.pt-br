---
description: As constantes de sinalizador de bits PHONEBUTTONMODE \_ descrevem as classes de botão.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: PHONEBUTTONMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761298"
---
# <a name="phonebuttonmode_-constants"></a>Constantes PHONEBUTTONMODE \_

As constantes de sinalizador de bits **PHONEBUTTONMODE \_** descrevem as classes de botão.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**CHAMADA \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



O botão é atribuído a uma aparência de chamada.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**EXIBIÇÃO \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



O botão é um botão "soft" associado à exibição do telefone. Um conjunto de telefone pode ter zero ou mais botões de exibição.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ FICTÍCIO**
</dt> <dd> <dl> <dt>



Esse valor é usado para descrever uma posição de botão/lâmpada que não tem nenhum botão correspondente, mas tem apenas uma lâmpada.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**RECURSO \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



O botão é atribuído à solicitação de recursos da opção, como espera, conferência e transferência.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE \_ KEYPAD**
</dt> <dd> <dl> <dt>



O botão é um dos doze botões do teclado, 0 a 9, \* ' ' e ' \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ LOCAL**
</dt> <dd> <dl> <dt>



O botão é um botão de função local, como mute ou controle de volume.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

Esse tipo de enumeração é usado na estrutura [**de dados PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) para descrever o significado associado aos botões do telefone.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




