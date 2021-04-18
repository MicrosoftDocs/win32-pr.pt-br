---
description: As \_ constantes de sinalizador de bit LINEADDRCAPFLAGS são usadas no membro dwAddrCapFlags da estrutura de dados LINEADDRESSCAPS para descrever vários recursos de endereço booliano.
ms.assetid: 530af273-82ba-4310-8aac-266d657e1bfe
title: Constantes de LINEADDRCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce6c8bebb5683d5ecb7d576ff7d376ad0d62cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788054"
---
# <a name="lineaddrcapflags_-constants"></a>\_Constantes LINEADDRCAPFLAGS

As  \_ constantes de sinalizador de bit LINEADDRCAPFLAGS são usadas no membro **dwAddrCapFlags** da estrutura de dados [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) para descrever vários recursos de endereço booliano.

<dl> <dt>

<span id="LINEADDRCAPFLAGS_ACCEPTTOALERT"></span><span id="lineaddrcapflags_accepttoalert"></span>**LINEADDRCAPFLAGS \_ ACCEPTTOALERT**
</dt> <dd> <dl> <dt>



**True** se uma chamada de oferta precisar ser aceita usando [**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept) para iniciar o alerta dos usuários em ambas as extremidades da chamada; caso contrário, **false**. Normalmente, isso é usado apenas com o ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ACDGROUP"></span><span id="lineaddrcapflags_acdgroup"></span>**LINEADDRCAPFLAGS \_ ACDGROUP**
</dt> <dd> <dl> <dt>



O endereço dá suporte a [grupos ad](about-call-center-controls.md#acd-group-object) em conexão com operações do Call Center. Consulte [sobre controles do Call Center](./about-call-center-controls.md) para obter informações adicionais sobre grupos de AD.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_AUTORECONNECT"></span><span id="lineaddrcapflags_autoreconnect"></span>**LINEADDRCAPFLAGS \_ falha**
</dt> <dd> <dl> <dt>



Especifica se a remoção de uma chamada de consulta é reconectada automaticamente à chamada em caso de controle de consulta. **True** se a reconexão ocorrer automaticamente; caso contrário, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDDEFAULT"></span><span id="lineaddrcapflags_blockiddefault"></span>**LINEADDRCAPFLAGS \_ BLOCKIDDEFAULT**
</dt> <dd> <dl> <dt>



Especifica se a rede, por padrão, envia ou bloqueia informações de ID do chamador ao fazer uma chamada nesse endereço. Se **for true**, as informações do identificador serão bloqueadas por padrão; Se **for false**, as informações do identificador serão transmitidas por padrão.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_BLOCKIDOVERRIDE"></span><span id="lineaddrcapflags_blockidoverride"></span>**LINEADDRCAPFLAGS \_ BLOCKIDOVERRIDE**
</dt> <dd> <dl> <dt>



Especifica se a configuração padrão para enviar ou bloquear informações de ID do chamador pode ser substituída por chamada. Se for **true**, a substituição será possível; Se for **false**, Override não será possível.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_COMPLETIONID"></span><span id="lineaddrcapflags_completionid"></span>**conclusão de LINEADDRCAPFLAGS \_**
</dt> <dd> <dl> <dt>



Especifica se os identificadores de conclusão retornados por [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall) são úteis e exclusivos. **True se for** útil; caso contrário, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFDROP"></span><span id="lineaddrcapflags_confdrop"></span>**LINEADDRCAPFLAGS \_ CONFDROP**
</dt> <dd> <dl> <dt>



**True** se [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) em um pai de chamada de conferência também tiver o efeito colateral de descartar (ou seja, desconectar) as outras partes envolvidas na chamada de conferência; **False** se o descarte de uma chamada de conferência ainda permitir que outras partes se comuniquem entre si.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEHELD"></span><span id="lineaddrcapflags_conferenceheld"></span>**LINEADDRCAPFLAGS \_ CONFERENCEHELD**
</dt> <dd> <dl> <dt>



Especifica se uma chamada Hard-retida pode ser conferência. Geralmente, somente chamadas de controle de consulta podem ser adicionadas como uma chamada de conferência.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_CONFERENCEMAKE"></span><span id="lineaddrcapflags_conferencemake"></span>**LINEADDRCAPFLAGS \_ CONFERENCEMAKE**
</dt> <dd> <dl> <dt>



Especifica se uma chamada totalmente nova pode ser estabelecida para uso como uma chamada de consulta (para adicionar) na conferência.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DESTOFFHOOK"></span><span id="lineaddrcapflags_destoffhook"></span>**LINEADDRCAPFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica se o telefone da parte chamada pode ser automaticamente forçado a offhook ao fazer chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_DIALED"></span><span id="lineaddrcapflags_dialed"></span>**LINEADDRCAPFLAGS \_ discado**
</dt> <dd> <dl> <dt>



Especifica se um endereço de destino pode ser discado nesse endereço para fazer uma chamada. **True** se um endereço de destino precisar ser discado; **False** se o endereço de destino for fixo (como com um "telefone ativo").


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDBUSYNAADDR"></span><span id="lineaddrcapflags_fwdbusynaaddr"></span>**LINEADDRCAPFLAGS \_ FWDBUSYNAADDR**
</dt> <dd> <dl> <dt>



Especifica se o encaminhamento de chamada para ocupado e sem resposta pode usar endereços de encaminhamento diferentes. Esse sinalizador só é significativo se o encaminhamento para ocupado e sem resposta puder ser controlado separadamente. Esse sinalizador será **verdadeiro** se o encaminhamento ficar ocupado e nenhuma resposta puder usar endereços de destino diferentes; caso contrário, será **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDCONSULT"></span><span id="lineaddrcapflags_fwdconsult"></span>**LINEADDRCAPFLAGS \_ FWDCONSULT**
</dt> <dd> <dl> <dt>



Especifica se o encaminhamento de chamada envolve o estabelecimento de uma chamada de consulta.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDINTEXTADDR"></span><span id="lineaddrcapflags_fwdintextaddr"></span>**LINEADDRCAPFLAGS \_ FWDINTEXTADDR**
</dt> <dd> <dl> <dt>



Especifica se chamadas internas e externas podem ser encaminhadas para endereços de encaminhamento diferentes. Esse sinalizador só será significativo se o encaminhamento de chamadas internas e externas puder ser controlado separadamente. Esse sinalizador será **verdadeiro** se chamadas internas e externas puderem ser encaminhadas para endereços de destino diferentes; caso contrário, será **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDNUMRINGS"></span><span id="lineaddrcapflags_fwdnumrings"></span>**LINEADDRCAPFLAGS \_ FWDNUMRINGS**
</dt> <dd> <dl> <dt>



Especifica se o número de anéis para uma não resposta pode ser especificado ao encaminhar chamadas sem resposta. Se for **true**, o intervalo válido será fornecido nos membros **dwMinFwdNumRings** e **dwMaxFwdNumRings** da estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_FWDSTATUSVALID"></span><span id="lineaddrcapflags_fwdstatusvalid"></span>**LINEADDRCAPFLAGS \_ FWDSTATUSVALID**
</dt> <dd> <dl> <dt>



Especifica se o status de encaminhamento na estrutura [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) para esse endereço é válido ou é no máximo uma "melhor estimativa", dada a ausência de uma confirmação precisa pelo comutador ou pela rede.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_HOLDMAKESNEW"></span><span id="lineaddrcapflags_holdmakesnew"></span>**LINEADDRCAPFLAGS \_ HOLDMAKESNEW**
</dt> <dd> <dl> <dt>



Quando uma chamada nesse endereço é colocada em espera (usando [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) ou ação externa), uma nova chamada é criada automaticamente (muito provavelmente em LINECALLSTATE de sinal de discagem \_ ).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOEXTERNALCALLS"></span><span id="lineaddrcapflags_noexternalcalls"></span>**LINEADDRCAPFLAGS \_ NOEXTERNALCALLS**
</dt> <dd> <dl> <dt>



O endereço é associado a uma linha interna em um PBX que é restrito de forma que ele não possa ser usado para fazer chamadas para um endereço fora do comutador (por exemplo, é um intercomunicador). O aplicativo pode usar essa indicação para ajudar o usuário a selecionar a aparência de chamada correta a ser usada para fazer uma chamada. Quando esse bit está desativado, ele não indica necessariamente que o endereço pode ser usado para fazer chamadas externas, pois o provedor de serviços não pode ser Cognizant do tipo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOINTERNALCALLS"></span><span id="lineaddrcapflags_nointernalcalls"></span>**LINEADDRCAPFLAGS \_ NOINTERNALCALLS**
</dt> <dd> <dl> <dt>



O endereço é associado a uma colinha direta (tronco) e não pode ser usado para fazer chamadas internas em um PBX. O aplicativo pode usar essa indicação para ajudar o usuário a selecionar a aparência de chamada correta a ser usada para fazer uma chamada. Quando esse bit está desativado, ele não indica necessariamente que o endereço pode ser usado para fazer chamadas internas, pois o provedor de serviços não pode ser Cognizant do tipo de linha.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_NOPSTNADDRESSTRANSLATION"></span><span id="lineaddrcapflags_nopstnaddresstranslation"></span>**LINEADDRCAPFLAGS \_ NOPSTNADDRESSTRANSLATION**
</dt> <dd> <dl> <dt>



Esse endereço não dá suporte à conversão de endereço de rede de telefone comutado público. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ORIGOFFHOOK"></span><span id="lineaddrcapflags_origoffhook"></span>**LINEADDRCAPFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



Especifica se o telefone da parte originadora pode ser automaticamente levado a offhook ao fazer chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PARTIALDIAL"></span><span id="lineaddrcapflags_partialdial"></span>**LINEADDRCAPFLAGS \_ PARTIALDIAL**
</dt> <dd> <dl> <dt>



Especifica se a discagem parcial está disponível.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPCALLWAIT"></span><span id="lineaddrcapflags_pickupcallwait"></span>**LINEADDRCAPFLAGS \_ PICKUPCALLWAIT**
</dt> <dd> <dl> <dt>



**True** se [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) puder ser usado para pegar uma chamada detectada pelo usuário como chamada em espera de chamada; caso contrário, **false**.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PICKUPGROUPID"></span><span id="lineaddrcapflags_pickupgroupid"></span>**LINEADDRCAPFLAGS \_ PICKUPGROUPID**
</dt> <dd> <dl> <dt>



Especifica se um identificador de grupo é necessário para a retirada de chamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_PREDICTIVEDIALER"></span><span id="lineaddrcapflags_predictivedialer"></span>**LINEADDRCAPFLAGS \_ PREDICTIVEDIALER**
</dt> <dd> <dl> <dt>



Esse endereço tem recursos de monitoramento de progresso de chamada aprimorados que podem ser aplicados a chamadas de saída para determinar Estados de chamada como de *toque*, *ocupado*, *specialinfo* e *conectado*, ou o tipo de mídia do dispositivo que responde à chamada. Ele também pode ter a capacidade de transferir automaticamente chamadas de saída para outro endereço quando uma chamada atinge qualquer um conjunto predefinido de Estados.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_QUEUE"></span><span id="lineaddrcapflags_queue"></span>**LINEADDRCAPFLAGS \_ fila**
</dt> <dd> <dl> <dt>



Esse endereço não está associado a uma estação ou dispositivo físico específico, mas é um local de retenção onde chamadas aguardam processamento adicional. As chamadas colocadas na fila podem receber um determinado tratamento. Eles também podem ser transferidos automaticamente quando um recurso específico se tornar disponível (por exemplo, se a fila for uma fila AD e as chamadas estiverem aguardando um agente disponível).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_ROUTEPOINT"></span><span id="lineaddrcapflags_routepoint"></span>**LINEADDRCAPFLAGS \_ ROUTEPOINT**
</dt> <dd> <dl> <dt>



Esse endereço não está associado a uma estação ou dispositivo físico específico, mas é um local de retenção onde chamadas aguardam o roteamento pelo aplicativo (o aplicativo examina o endereço chamado e pode redirecionar a chamada para outro endereço). A chamada também pode ser transferida automaticamente se um tempo limite de roteamento expirar (a opção geralmente assume um roteamento padrão).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SECURE"></span><span id="lineaddrcapflags_secure"></span>**LINEADDRCAPFLAGS \_ seguro**
</dt> <dd> <dl> <dt>



Especifica se as chamadas nesse endereço podem se tornar seguras no momento da configuração da chamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETCALLINGID"></span><span id="lineaddrcapflags_setcallingid"></span>**LINEADDRCAPFLAGS \_ SETchamáid**
</dt> <dd> <dl> <dt>



O aplicativo pode optar por definir o membro **CallingPartyID** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) ao chamar [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) e outras funções que aceitam uma estrutura **LINECALLPARAMS** . O provedor de serviço, se o conteúdo do identificador for aceitável e um caminho estiver disponível, passará o identificador para a parte chamada para indicar a identidade da entidade de chamada.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_SETUPCONFNULL"></span><span id="lineaddrcapflags_setupconfnull"></span>**LINEADDRCAPFLAGS \_ SETUPCONFNULL**
</dt> <dd> <dl> <dt>



Especifica se a configuração de uma chamada de conferência começa com uma chamada inicial (**false**) ou sem uma chamada inicial (**true**).


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERHELD"></span><span id="lineaddrcapflags_transferheld"></span>**LINEADDRCAPFLAGS \_ TRANSFERHELD**
</dt> <dd> <dl> <dt>



Especifica se uma chamada Hard-retida pode ser transferida. Geralmente, somente chamadas de controle de consulta podem ser transferidas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRCAPFLAGS_TRANSFERMAKE"></span><span id="lineaddrcapflags_transfermake"></span>**LINEADDRCAPFLAGS \_ TRANSFERMAKE**
</dt> <dd> <dl> <dt>



Especifica se uma chamada totalmente nova pode ser estabelecida para uso como uma chamada de consulta na transferência.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineAccept**](/windows/desktop/api/Tapi/nf-tapi-lineaccept)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

