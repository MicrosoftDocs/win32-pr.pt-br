---
title: Códigos de erro de animação do Windows (Winerror. h)
description: Se ocorrer um erro, a animação do Windows retornará um código como um valor HRESULT. Esta seção fornece uma lista de códigos de erro específicos da animação do Windows. Para obter uma lista de códigos de erro COM gerais, consulte códigos de erro COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788856"
---
# <a name="windows-animation-error-codes"></a>Códigos de erro de animação do Windows

Se ocorrer um erro, a animação do Windows retornará um código como um valor **HRESULT** . Esta seção fornece uma lista de códigos de erro específicos da animação do Windows. Para obter uma lista de códigos de erro COM gerais, consulte [códigos de erro com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**\_ \_ falha na criação da interface do usuário \_**
</dt> <dd> <dl> <dt>

0x802A0001
</dt> <dt>



Não foi possível criar o objeto.


</dt> </dl> </dd> <dt>

<span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**interface de usuário \_ E \_ desligamento \_ chamada**
</dt> <dd> <dl> <dt>

0x802A0002
</dt> <dt>



O método de [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) foi chamado no Gerenciador de animação, fazendo com que o Gerenciador de animação seja desligado e todas as variáveis de animação e Storyboards criados para serem liberados.

> [!Note]  
> Nenhum método pode ser chamado em qualquer objeto de animação após o [**desligamento**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).

 


</dt> </dl> </dd> <dt>

<span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**IU \_ E \_ \_ reentrância ilegal**
</dt> <dd> <dl> <dt>

0x802A0003
</dt> <dt>



Este método não pode ser chamado durante esse tipo de retorno de chamada.


</dt> </dl> </dd> <dt>

<span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI \_ E \_ objeto \_ lacrado**
</dt> <dd> <dl> <dt>

0x802A0004
</dt> <dt>



Este objeto foi lacrado, portanto, essa alteração não é mais permitida.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**valor de IU \_ E \_ \_ não \_ definido**
</dt> <dd> <dl> <dt>

0x802A0005
</dt> <dt>



O valor solicitado nunca foi definido e, portanto, não pode ser recuperado.


</dt> </dl> </dd> <dt>

<span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**valor de IU \_ E \_ \_ não \_ determinado**
</dt> <dd> <dl> <dt>

0x802A0006
</dt> <dt>



O valor solicitado não pode ser determinado.


</dt> </dl> </dd> <dt>

<span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**saída de interface de usuário \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

0x802A0007
</dt> <dt>



Um retorno de chamada retornou um parâmetro de saída inválido.


</dt> </dl> </dd> <dt>

<span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**interface do usuário \_ E \_ booliano \_ esperado**
</dt> <dd> <dl> <dt>

0x802A0008
</dt> <dt>



Um retorno de chamada retornou um código de êxito diferente de S \_ OK ou s \_ false.


</dt> </dl> </dd> <dt>

<span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**IU \_ E \_ \_ proprietário diferente**
</dt> <dd> <dl> <dt>

0x802A0009
</dt> <dt>



Um parâmetro que deve pertencer a esse objeto pertence a um objeto diferente.


</dt> </dl> </dd> <dt>

<span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**\_ \_ correspondência ambígua E de interface do usuário \_**
</dt> <dd> <dl> <dt>

0x802A000A
</dt> <dt>



Mais de um item correspondeu aos critérios de pesquisa.


</dt> </dl> </dd> <dt>

<span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**estouro de IU \_ E \_ FP \_**
</dt> <dd> <dl> <dt>

0x802A000B
</dt> <dt>



Ocorreu um estouro de ponto flutuante.


</dt> </dl> </dd> <dt>

<span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**interface de usuário \_ E \_ thread incorreto \_**
</dt> <dd> <dl> <dt>

0x802A000C
</dt> <dt>



Esse método só pode ser chamado a partir do thread que criou o objeto.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**interface do usuário \_ E \_ storyboard \_ ativa**
</dt> <dd> <dl> <dt>

0x802A0101
</dt> <dt>



O storyboard está atualmente na agenda.


</dt> </dl> </dd> <dt>

<span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**a interface do usuário \_ E o \_ Storyboard não estão em \_ \_ execução**
</dt> <dd> <dl> <dt>

0x802A0102
</dt> <dt>



O storyboard não está sendo reproduzido.


</dt> </dl> </dd> <dt>

<span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**IU \_ E \_ \_ quadro-chave inicial após o \_ \_ final**
</dt> <dd> <dl> <dt>

0x802A0103
</dt> <dt>



O quadro-chave inicial pode ocorrer após o quadro-chave final.


</dt> </dl> </dd> <dt>

<span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**quadro-chave de término da interface do usuário \_ \_ \_ \_ não \_ determinado**
</dt> <dd> <dl> <dt>

0x802A0104
</dt> <dt>



Pode não ser possível determinar a hora do quadro-chave final quando o quadro chave inicial é atingido.


</dt> </dl> </dd> <dt>

<span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**sobreposição de \_ \_ loops E de interface do usuário \_**
</dt> <dd> <dl> <dt>

0x802A0105
</dt> <dt>



Duas partes repetidas de um storyboard podem se sobrepor.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**interface do usuário \_ E \_ transição \_ já \_ usada**
</dt> <dd> <dl> <dt>

0x802A0106
</dt> <dt>



A transição já foi adicionada a um storyboard diferente ou foi adicionada a um Storyboard que terminou de ser reproduzido e liberada.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**a \_ transição de interface do usuário E \_ não está \_ \_ no \_ storyboard**
</dt> <dd> <dl> <dt>

0x802A0107
</dt> <dt>



A transição não foi adicionada a nenhum Storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transição de interface do usuário \_ E \_ \_ Eclipse**
</dt> <dd> <dl> <dt>

0x802A0108
</dt> <dt>



A transição pode ocultar o início de outra transição no storyboard.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**\_tempo E \_ hora da IU antes da \_ \_ última \_ atualização**
</dt> <dd> <dl> <dt>

0x802A0109
</dt> <dt>



A hora especificada é anterior à hora passada para a última atualização.


</dt> </dl> </dd> <dt>

<span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_cliente do temporizador E de interface do usuário \_ \_ \_ já \_ conectado**
</dt> <dd> <dl> <dt>

0x802A010A
</dt> <dt>



Este cliente já está conectado a um temporizador.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista e atualização de plataforma para aplicativos de área de trabalho do Windows Vista \[ somente\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                       |
| parâmetro<br/>                   | <dl> <dt>Winerror. h</dt> </dl>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de animação do Windows](windows-animation-reference.md)
</dt> </dl>

 

