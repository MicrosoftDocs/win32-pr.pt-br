---
description: As \_ constantes de sinalizador de bit LINEDEVSTATUSFLAGS descrevem uma coleção de itens de status de dispositivo de linha booliana.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes de LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764758"
---
# <a name="linedevstatusflags_-constants"></a>\_Constantes LINEDEVSTATUSFLAGS

As constantes de sinalizador de bit **LINEDEVSTATUSFLAGS \_** descrevem uma coleção de itens de status de dispositivo de linha booliana.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ conectado**
</dt> <dd> <dl> <dt>



Especifica se a linha está conectada à TAPI. Se for **true**, a linha será conectada e a TAPI será capaz de operar no dispositivo de linha. Se for **false**, a linha será desconectada e o aplicativo não poderá controlar o dispositivo de linha por meio da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INserviço**
</dt> <dd> <dl> <dt>



Indica se a linha está em serviço. Se for **true**, a linha estará em serviço; Se for **false**, a linha estará fora do serviço.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloqueado**
</dt> <dd> <dl> <dt>



Indica se a linha está bloqueada ou desbloqueada. Esse bit é usado com mais frequência com dispositivos de linha associados a telefones celulares. Muitos telefones celulares têm um mecanismo de segurança que exige a entrada de uma senha para permitir que o telefone faça chamadas. Esse bit pode ser usado para indicar aos aplicativos que o telefone está bloqueado e não pode fazer chamadas até que a senha seja inserida na interface do usuário do telefone para que o aplicativo possa apresentar um alerta apropriado ao usuário.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Indica se a linha tem uma mensagem aguardando. Se for **true**, uma mensagem estará aguardando; Se for **false**, nenhuma mensagem estará aguardando.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

\_As constantes LINEDEVSTATUSFLAGS são usadas dentro do membro **dwDevStatusFlags** da estrutura de dados [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




