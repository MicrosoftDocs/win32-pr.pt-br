---
description: Veja a seguir uma lista de códigos de erro que a TAPI pode retornar ao invocar operações em linhas, endereços ou chamadas.
ms.assetid: bdaf60d1-6ff2-4bd6-b246-8556d6cae644
title: Constantes de LINEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ed7757377d26dbde832b7ef50f275b45e21760d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780120"
---
# <a name="lineerr_-constants"></a>\_Constantes LINEERR

Veja a seguir uma lista de códigos de erro que a TAPI pode retornar ao invocar operações em linhas, endereços ou chamadas. Para obter mais informações sobre como determinar quais desses códigos de erro uma função específica pode retornar, consulte as descrições de função individuais.

<dl> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



O endereço especificado está impedido de ser discado na chamada especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ADDRESSBLOCKED"></span><span id="lineerr_addressblocked"></span>**LINEERR \_ ADDRESSBLOCKED**
</dt> <dd> <dl> <dt>



O endereço de chamada de destino tem bloqueio de chamada habilitado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_ALLOCATED"></span><span id="lineerr_allocated"></span>**LINEERR \_ alocada**
</dt> <dd> <dl> <dt>



A linha não pode ser aberta devido a uma condição persistente, como a de uma porta serial que está sendo aberta exclusivamente por outro processo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BADDEVICEID"></span><span id="lineerr_baddeviceid"></span>**LINEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



O identificador de dispositivo ou o identificador de dispositivo de linha especificado, como em um parâmetro *dwDeviceID* , é inválido ou está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BEARERMODEUNAVAIL"></span><span id="lineerr_bearermodeunavail"></span>**LINEERR \_ BEARERMODEUNAVAIL**
</dt> <dd> <dl> <dt>



O membro do modo de portador em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) é inválido, o modo de portador especificado em **LINECALLPARAMS** não está disponível ou o modo de portador de chamada não pode ser alterado para o modo de portador especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_BILLINGREJECTED"></span><span id="lineerr_billingrejected"></span>**LINEERR \_ BILLINGREJECTED**
</dt> <dd> <dl> <dt>



O modo de cobrança da chamada foi rejeitado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CALLUNAVAIL"></span><span id="lineerr_callunavail"></span>**LINEERR \_ CALLUNAVAIL**
</dt> <dd> <dl> <dt>



Todas as aparências de chamada no endereço especificado estão em uso no momento.


</dt> </dl> </dd> <dt>

<span id="LINEERR_COMPLETIONOVERRUN"></span><span id="lineerr_completionoverrun"></span>**LINEERR \_ COMPLETIONOVERRUN**
</dt> <dd> <dl> <dt>



O número máximo de conclusões de chamadas pendentes foi excedido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_CONFERENCEFULL"></span><span id="lineerr_conferencefull"></span>**LINEERR \_ CONFERENCEFULL**
</dt> <dd> <dl> <dt>



O número máximo de partes de uma conferência foi atingido ou o número de partes solicitado não pode ser satisfeito.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALBILLING"></span><span id="lineerr_dialbilling"></span>**LINEERR \_ DIALBILLING**
</dt> <dd> <dl> <dt>



O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALDIALTONE"></span><span id="lineerr_dialdialtone"></span>**LINEERR \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>



O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALPROMPT"></span><span id="lineerr_dialprompt"></span>**LINEERR \_ DIALPROMPT**
</dt> <dd> <dl> <dt>



O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALQUIET"></span><span id="lineerr_dialquiet"></span>**LINEERR \_ DIALQUIET**
</dt> <dd> <dl> <dt>



O parâmetro endereço discável contém caracteres de controle de discagem não processados pelo provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DIALVOICEDETECT"></span><span id="lineerr_dialvoicedetect"></span>**LINEERR \_ DIALVOICEDETECT**
</dt> <dd> <dl> <dt>



Uso do modificador de discagem (:) Não tem suporte. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_DISCONNECTED"></span><span id="lineerr_disconnected"></span>**LINEERR \_ desconectado**
</dt> <dd> <dl> <dt>



A chamada foi desconectada. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEAPIVERSION"></span><span id="lineerr_incompatibleapiversion"></span>**LINEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



O aplicativo solicitou uma versão TAPI ou um intervalo de versão que seja incompatível com o, ou que não tenha suporte do, a implementação da API de telefonia e o provedor de serviços correspondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INCOMPATIBLEEXTVERSION"></span><span id="lineerr_incompatibleextversion"></span>**LINEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



O aplicativo solicitou um intervalo de versão de extensão inválido ou não tem suporte do provedor de serviços correspondente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INIFILECORRUPT"></span><span id="lineerr_inifilecorrupt"></span>**LINEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



O arquivo de Telephon.ini não pode ser lido ou compreendido corretamente pela TAPI devido a inconsistências internas ou problemas de formatação. Por exemplo, a \[ \] seção locais, \[ cartões \] ou \[ países \] do arquivo de Telephon.ini pode estar corrompida ou inconsistente.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INUSE"></span><span id="lineerr_inuse"></span>**LINEERR \_ INUSE**
</dt> <dd> <dl> <dt>



O dispositivo de linha está em uso e não pode ser configurado no momento, permitir que uma parte seja adicionada, permitir que uma chamada seja respondida, permitir que uma chamada seja colocada ou permitir que uma chamada seja transferida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESS"></span><span id="lineerr_invaladdress"></span>**LINEERR \_ INVALADDRESS**
</dt> <dd> <dl> <dt>



Um endereço especificado é inválido ou não é permitido. Se for inválido, o endereço contém caracteres ou dígitos inválidos ou o endereço de destino contém caracteres de controle de discagem (W, @, $ ou?) que não são suportados pelo provedor de serviços. Se não for permitido, o endereço especificado não será atribuído à linha especificada ou não será válido para o redirecionamento de endereço.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSID"></span><span id="lineerr_invaladdressid"></span>**LINEERR \_ INVALADDRESSID**
</dt> <dd> <dl> <dt>



O identificador de endereço especificado é inválido ou está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSMODE"></span><span id="lineerr_invaladdressmode"></span>**LINEERR \_ INVALADDRESSMODE**
</dt> <dd> <dl> <dt>



O modo de endereço especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSSTATE"></span><span id="lineerr_invaladdressstate"></span>**LINEERR \_ INVALADDRESSSTATE**
</dt> <dd> <dl> <dt>



O estado de endereço especificado contém um ou mais bits que não [**são \_ constantes LINEADDRESSSTATE**](lineaddressstate--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALADDRESSTYPE"></span><span id="lineerr_invaladdresstype"></span>**LINEERR \_ INVALADDRESSTYPE**
</dt> <dd> <dl> <dt>



O aplicativo referenciou um tipo de endereço que não é válido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 3,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



A atividade do agente especificada não é válida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTACTIVITY"></span><span id="lineerr_invalagentactivity"></span>**LINEERR \_ INVALAGENTACTIVITY**
</dt> <dd> <dl> <dt>



O aplicativo que invoca essa operação é o destino da entrega indireta. Ou seja, a TAPI determinou que o aplicativo de chamada também é o aplicativo de prioridade mais alta para o tipo de mídia fornecido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



As informações do grupo de agentes especificadas não são válidas ou contêm erros. A ação solicitada não foi executada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTGROUP"></span><span id="lineerr_invalagentgroup"></span>**LINEERR \_ INVALAGENTGROUP**
</dt> <dd> <dl> <dt>



O aplicativo referenciou um grupo de agentes que não é válido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



O identificador de agente especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTID"></span><span id="lineerr_invalagentid"></span>**LINEERR \_ INVALAGENTID**
</dt> <dd> <dl> <dt>



Foi usado um identificador de agente inválido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSESSIONSTATE"></span><span id="lineerr_invalagentsessionstate"></span>**LINEERR \_ INVALAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



O estado da sessão do agente é inválido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



O estado do agente especificado não é válido ou contém erros. Nenhuma alteração foi feita no estado do agente do endereço especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAGENTSTATE"></span><span id="lineerr_invalagentstate"></span>**LINEERR \_ INVALAGENTSTATE**
</dt> <dd> <dl> <dt>



O aplicativo referenciou um estado de agente que não é válido. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPHANDLE"></span><span id="lineerr_invalapphandle"></span>**LINEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



O identificador do aplicativo (como especificado por um parâmetro *hLineApp* ) ou o identificador de registro do aplicativo é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALAPPNAME"></span><span id="lineerr_invalappname"></span>**LINEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



O nome do aplicativo especificado é inválido. Se um nome de aplicativo for especificado pelo aplicativo, supõe-se que a cadeia de caracteres não contém nenhum caractere não-reproduzido e terminada com zero.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALBEARERMODE"></span><span id="lineerr_invalbearermode"></span>**LINEERR \_ INVALBEARERMODE**
</dt> <dd> <dl> <dt>



O modo de portador especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLCOMPLMODE"></span><span id="lineerr_invalcallcomplmode"></span>**LINEERR \_ INVALCALLCOMPLMODE**
</dt> <dd> <dl> <dt>



A conclusão especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLHANDLE"></span><span id="lineerr_invalcallhandle"></span>**LINEERR \_ INVALCALLHANDLE**
</dt> <dd> <dl> <dt>



O identificador de chamada especificado não é válido. Por exemplo, o identificador não é **nulo** , mas não pertence à linha especificada. Em alguns casos, o identificador do dispositivo de chamada especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPARAMS"></span><span id="lineerr_invalcallparams"></span>**LINEERR \_ INVALCALLPARAMS**
</dt> <dd> <dl> <dt>



Os parâmetros de chamada especificados são inválidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLPRIVILEGE"></span><span id="lineerr_invalcallprivilege"></span>**LINEERR \_ INVALCALLPRIVILEGE**
</dt> <dd> <dl> <dt>



O parâmetro de privilégio de chamada especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSELECT"></span><span id="lineerr_invalcallselect"></span>**LINEERR \_ INVALCALLSELECT**
</dt> <dd> <dl> <dt>



O parâmetro Select especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATE"></span><span id="lineerr_invalcallstate"></span>**LINEERR \_ INVALCALLSTATE**
</dt> <dd> <dl> <dt>



O estado atual de uma chamada não está em um estado válido para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCALLSTATELIST"></span><span id="lineerr_invalcallstatelist"></span>**LINEERR \_ INVALCALLSTATELIST**
</dt> <dd> <dl> <dt>



A lista de Estados da chamada especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCARD"></span><span id="lineerr_invalcard"></span>**LINEERR \_ INVALCARD**
</dt> <dd> <dl> <dt>



O identificador de cartão permanente especificado em *dwCard* não pôde ser encontrado em nenhuma entrada na \[ seção de cartões \] no registro.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOMPLETIONID"></span><span id="lineerr_invalcompletionid"></span>**LINEERR \_ INVALCOMPLETIONID**
</dt> <dd> <dl> <dt>



O identificador de conclusão é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONFCALLHANDLE"></span><span id="lineerr_invalconfcallhandle"></span>**LINEERR \_ INVALCONFCALLHANDLE**
</dt> <dd> <dl> <dt>



O identificador de chamada especificado para a chamada de conferência é inválido ou não é um identificador para uma chamada de conferência.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCONSULTCALLHANDLE"></span><span id="lineerr_invalconsultcallhandle"></span>**LINEERR \_ INVALCONSULTCALLHANDLE**
</dt> <dd> <dl> <dt>



O identificador de chamada de consulta especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALCOUNTRYCODE"></span><span id="lineerr_invalcountrycode"></span>**LINEERR \_ INVALCOUNTRYCODE**
</dt> <dd> <dl> <dt>



O código de país ou região especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICECLASS"></span><span id="lineerr_invaldeviceclass"></span>**LINEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



O dispositivo de linha não tem dispositivo associado para a classe de dispositivo fornecida ou a linha especificada não oferece suporte à classe de dispositivo indicada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDEVICEHANDLE"></span><span id="lineerr_invaldevicehandle"></span>**LINEERR \_ INVALDEVICEHANDLE**
</dt> <dd> <dl> <dt>



O identificador do dispositivo de linha é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIALPARAMS"></span><span id="lineerr_invaldialparams"></span>**LINEERR \_ INVALDIALPARAMS**
</dt> <dd> <dl> <dt>



Os parâmetros de discagem são inválidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITLIST"></span><span id="lineerr_invaldigitlist"></span>**LINEERR \_ INVALDIGITLIST**
</dt> <dd> <dl> <dt>



A lista de dígitos especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITMODE"></span><span id="lineerr_invaldigitmode"></span>**LINEERR \_ INVALDIGITMODE**
</dt> <dd> <dl> <dt>



O modo de dígito especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALDIGITS"></span><span id="lineerr_invaldigits"></span>**LINEERR \_ INVALDIGITS**
</dt> <dd> <dl> <dt>



Os dígitos de terminação especificados não são válidos.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALEXTVERSION"></span><span id="lineerr_invalextversion"></span>**LINEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



O número de versão da extensão do provedor de serviços é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



O parâmetro *dwFeature* é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALFEATURE"></span><span id="lineerr_invalfeature"></span>**LINEERR \_ INVALFEATURE**
</dt> <dd> <dl> <dt>



O aplicativo invocou um recurso que não está disponível nesta linha.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALGROUPID"></span><span id="lineerr_invalgroupid"></span>**LINEERR \_ INVALGROUPID**
</dt> <dd> <dl> <dt>



O identificador de grupo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINEHANDLE"></span><span id="lineerr_invallinehandle"></span>**LINEERR \_ INVALLINEHANDLE**
</dt> <dd> <dl> <dt>



A chamada, o dispositivo, o dispositivo de linha ou o identificador de linha especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLINESTATE"></span><span id="lineerr_invallinestate"></span>**LINEERR \_ INVALLINESTATE**
</dt> <dd> <dl> <dt>



A configuração do dispositivo não pode ser alterada no estado de linha atual. A linha pode estar em uso por outro aplicativo ou um parâmetro *dwLineStates* contém um ou mais bits que não são [ \_ constantes LINEDEVSTATE](linedevstate--constants.md). O **valor \_ INVALLINESTATE de LINEERR** também pode indicar que o dispositivo está desconectado ou fora do serviço. Esses Estados são indicados pela configuração dos bits correspondentes aos valores de *InLINEDEVSTATUSFLAGS \_ conectados* e *LINEDEVSTATUSFLAGS \_ InService* para 0 no membro **DwDevStatusFlags** da estrutura [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) retornada pela função [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALLOCATION"></span><span id="lineerr_invallocation"></span>**LINEERR \_ INVALLOCATION**
</dt> <dd> <dl> <dt>



O identificador de local permanente especificado em *dwLocation* não foi encontrado em nenhuma entrada na \[ seção locais \] no registro.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIALIST"></span><span id="lineerr_invalmedialist"></span>**LINEERR \_ INVALMEDIALIST**
</dt> <dd> <dl> <dt>



A lista de mídias especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMEDIAMODE"></span><span id="lineerr_invalmediamode"></span>**LINEERR \_ INVALMEDIAMODE**
</dt> <dd> <dl> <dt>



A lista de tipos de mídia (modos) a serem monitorados contém informações inválidas, o parâmetro de tipo de mídia especificado é inválido ou o provedor de serviços não oferece suporte ao tipo de mídia especificado. Os tipos de mídia com suporte na linha são listados no membro **dwMediaModes** na estrutura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALMESSAGEID"></span><span id="lineerr_invalmessageid"></span>**LINEERR \_ INVALMESSAGEID**
</dt> <dd> <dl> <dt>



O número fornecido em *dwMessageID* está fora do intervalo especificado pelo membro **DwNumCompletionMessages** na estrutura [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARAM"></span><span id="lineerr_invalparam"></span>**LINEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Um parâmetro ou uma estrutura que um parâmetro aponta para conter informações inválidas, um país ou código de região inválido, um identificador de janela é inválido ou o parâmetro de lista de encaminhamento especificado contém informações inválidas.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKID"></span><span id="lineerr_invalparkid"></span>**LINEERR \_ INVALPARKID**
</dt> <dd> <dl> <dt>



O identificador de estacionamento é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPARKMODE"></span><span id="lineerr_invalparkmode"></span>**LINEERR \_ INVALPARKMODE**
</dt> <dd> <dl> <dt>



O modo de estacionamento especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



A senha especificada não está correta e a ação solicitada não foi executada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPASSWORD"></span><span id="lineerr_invalpassword"></span>**LINEERR \_ INVALPASSWORD**
</dt> <dd> <dl> <dt>



O aplicativo usou uma senha inválida. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,0 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPOINTER"></span><span id="lineerr_invalpointer"></span>**LINEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Um ou mais dos parâmetros de ponteiro especificados (como *lpCallList*, *lpdwAPIVersion*, *lpExtensionID*, *lpdwExtVersion*, *lphIcon*, *lpLineDevCaps* e *lpToneList*) são inválidos ou um ponteiro necessário para um parâmetro de saída é **nulo**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALPRIVSELECT"></span><span id="lineerr_invalprivselect"></span>**LINEERR \_ INVALPRIVSELECT**
</dt> <dd> <dl> <dt>



Um sinalizador inválido ou uma combinação de sinalizadores foi definida para o parâmetro *dwPrivileges* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALRATE"></span><span id="lineerr_invalrate"></span>**LINEERR \_ INVALRATE**
</dt> <dd> <dl> <dt>



A taxa especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALREQUESTMODE"></span><span id="lineerr_invalrequestmode"></span>**LINEERR \_ INVALREQUESTMODE**
</dt> <dd> <dl> <dt>



O indicador [**LINEREQUESTMODE**](linerequestmode--constants.md) é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALID"></span><span id="lineerr_invalterminalid"></span>**LINEERR \_ INVALTERMINALID**
</dt> <dd> <dl> <dt>



O identificador de terminal especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTERMINALMODE"></span><span id="lineerr_invalterminalmode"></span>**LINEERR \_ INVALTERMINALMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modos de terminal especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTIMEOUT"></span><span id="lineerr_invaltimeout"></span>**LINEERR \_ INVALTIMEOUT**
</dt> <dd> <dl> <dt>



Não há suporte para tempos limite ou um valor fica fora do intervalo válido especificado em [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps).


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONE"></span><span id="lineerr_invaltone"></span>**LINEERR \_ INVALTONE**
</dt> <dd> <dl> <dt>



O Tom personalizado especificado não representa um tom válido ou é composto de muitas frequências ou a estrutura de tons especificada não descreve um tom válido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONELIST"></span><span id="lineerr_invaltonelist"></span>**LINEERR \_ INVALTONELIST**
</dt> <dd> <dl> <dt>



A lista de tons especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTONEMODE"></span><span id="lineerr_invaltonemode"></span>**LINEERR \_ INVALTONEMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modo de Tom especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_INVALTRANSFERMODE"></span><span id="lineerr_invaltransfermode"></span>**LINEERR \_ INVALTRANSFERMODE**
</dt> <dd> <dl> <dt>



O parâmetro do modo de transferência especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_LINEMAPPERFAILED"></span><span id="lineerr_linemapperfailed"></span>**LINEERR \_ LINEMAPPERFAILED**
</dt> <dd> <dl> <dt>



LINEMAPPER foi o valor passado no parâmetro *dwDeviceID* , mas não foram encontradas linhas que correspondam aos requisitos especificados no parâmetro *lpCallParams* .


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOCONFERENCE"></span><span id="lineerr_noconference"></span>**LINEERR \_ NOconferência**
</dt> <dd> <dl> <dt>



A chamada especificada não é um identificador de chamada de conferência ou uma chamada de participante.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODEVICE"></span><span id="lineerr_nodevice"></span>**LINEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



O identificador de dispositivo especificado, que era válido anteriormente, não é mais aceito porque o dispositivo associado foi removido do sistema desde que a TAPI foi inicializada pela última vez. Como alternativa, o dispositivo de linha não tem nenhum dispositivo associado para a classe de dispositivo fornecida.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NODRIVER"></span><span id="lineerr_nodriver"></span>**LINEERR \_ NOunidade**
</dt> <dd> <dl> <dt>



Não foi possível localizar o Tapiaddr.dll ou o provedor de serviços de telefonia para o dispositivo especificado descobriu que um de seus componentes está ausente ou corrompido de uma forma que não foi detectada no momento da inicialização. O usuário deve ser aconselhado a usar o painel de controle de telefonia para corrigir o problema.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMEM"></span><span id="lineerr_nomem"></span>**nome do LINEERR \_**
</dt> <dd> <dl> <dt>



Memória insuficiente para executar a operação ou não é possível bloquear a memória.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Um provedor de serviços de telefonia que não dá suporte a várias instâncias é listado mais de uma vez \[ na \] seção de provedores no registro. O aplicativo deve aconselhar o usuário a usar o painel de controle de telefonia para remover o driver duplicado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOMULTIPLEINSTANCE"></span><span id="lineerr_nomultipleinstance"></span>**LINEERR \_ NOMULTIPLEINSTANCE**
</dt> <dd> <dl> <dt>



Várias instâncias deste provedor de serviços não são permitidas.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOREQUEST"></span><span id="lineerr_norequest"></span>**LINEERR \_ NOrequest**
</dt> <dd> <dl> <dt>



No momento, não há nenhuma solicitação pendente do modo indicado ou o aplicativo não é mais o aplicativo de prioridade mais alta para o modo de solicitação especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTOWNER"></span><span id="lineerr_notowner"></span>**LINEERR \_ NOcidade**
</dt> <dd> <dl> <dt>



O aplicativo não tem o privilégio de proprietário para a chamada especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_NOTREGISTERED"></span><span id="lineerr_notregistered"></span>**LINEERR não \_ registrado**
</dt> <dd> <dl> <dt>



O aplicativo não está registrado como um destinatário de solicitação para o modo de solicitação indicado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONFAILED"></span><span id="lineerr_operationfailed"></span>**LINEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



A operação falhou por um motivo desconhecido ou não especificado.


</dt> </dl> </dd> <dt>

<span id="LINEERR_OPERATIONUNAVAIL"></span><span id="lineerr_operationunavail"></span>**LINEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



A operação não está disponível, por exemplo, para o dispositivo especificado ou para a linha especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RATEUNAVAIL"></span><span id="lineerr_rateunavail"></span>**LINEERR \_ RATEUNAVAIL**
</dt> <dd> <dl> <dt>



O provedor de serviços atualmente não tem largura de banda suficiente disponível para a taxa especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialização do LINEERR \_**
</dt> <dd> <dl> <dt>



Se a reinicialização da TAPI tiver sido solicitada, por exemplo, como resultado da adição ou remoção de um provedor de serviços de telefonia, as solicitações [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize), [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)ou [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) serão rejeitadas com esse erro até que o último aplicativo desligue seu uso da API (usando [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)), quando a nova configuração entrar em vigor e os aplicativos forem novamente permitidos para chamar **lineInitialize** ou **lineInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REINIT"></span><span id="lineerr_reinit"></span>**reinicialização do LINEERR \_**
</dt> <dd> <dl> <dt>



O aplicativo tentou inicializar a TAPI duas vezes.


</dt> </dl> </dd> <dt>

<span id="LINEERR_REQUESTOVERRUN"></span><span id="lineerr_requestoverrun"></span>**LINEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



Mais solicitações estão pendentes que o dispositivo pode manipular.


</dt> </dl> </dd> <dt>

<span id="LINEERR_RESOURCEUNAVAIL"></span><span id="lineerr_resourceunavail"></span>**LINEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



Recursos insuficientes para concluir a operação. Por exemplo, uma linha não pode ser aberta devido a um sobrecompromisso de recurso dinâmico.


</dt> </dl> </dd> <dt>

<span id="LINEERR_STRUCTURETOOSMALL"></span><span id="lineerr_structuretoosmall"></span>**LINEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



O membro **dwTotalSize** de uma estrutura não especifica memória suficiente para conter a parte fixa da estrutura especificada.


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETNOTFOUND"></span><span id="lineerr_targetnotfound"></span>**LINEERR \_ TARGETNOTFOUND**
</dt> <dd> <dl> <dt>



Não foi encontrado um destino para a entrega de chamada. Isso pode ocorrer se o aplicativo nomeado não abriu a mesma linha com o bit do \_ proprietário LINECALLPRIVILEGE no parâmetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen). Ou, no caso de entrega no modo de mídia, nenhum aplicativo abriu a mesma linha com o bit do \_ proprietário LINECALLPRIVILEGE no parâmetro *DwPrivileges* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) e com o tipo de mídia especificado no parâmetro *DwMediaMode* que foi especificado no parâmetro *dwMediaModes* de [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen).


</dt> </dl> </dd> <dt>

<span id="LINEERR_TARGETSELF"></span><span id="lineerr_targetself"></span>**LINEERR \_ TARGETSELF**
</dt> <dd> <dl> <dt>



O aplicativo que invoca essa operação é o destino da entrega indireta. Ou seja, a TAPI determinou que o aplicativo de chamada também é o aplicativo de prioridade mais alta para o tipo de mídia fornecido.


</dt> </dl> </dd> <dt>

<span id="LINEERR_UNINITIALIZED"></span><span id="lineerr_uninitialized"></span>**LINEERR não \_ inicializado**
</dt> <dd> <dl> <dt>



A operação foi invocada antes de qualquer aplicativo chamado [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERCANCELLED"></span><span id="lineerr_usercancelled"></span>**LINEERR \_ USERcanceled**
</dt> <dd> <dl> <dt>



O usuário cancelou a chamada. Esse valor é exposto somente a aplicativos que negociam uma versão TAPI do 2,2 ou posterior.


</dt> </dl> </dd> <dt>

<span id="LINEERR_USERUSERINFOTOOBIG"></span><span id="lineerr_useruserinfotoobig"></span>**LINEERR \_ USERUSERINFOTOOBIG**
</dt> <dd> <dl> <dt>



A cadeia de caracteres que contém informações de usuário do usuário excede o número máximo de bytes especificado no membro **dwUUIAcceptSize**, **dwUUIAnswerSize**, **dwUUIDropSize**, **dwUUIMakeCallSize** ou **dwUUISendUserUserInfoSize** de [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps), ou a cadeia de caracteres que contém as informações do usuário do usuário é muito longa.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os valores de 0xC0000000 a 0xFFFFFFFF estão disponíveis para extensões específicas do dispositivo. Os valores 0x80000000 a 0xBFFFFFFF são reservados, enquanto 0x00000000 a 0x7FFFFFFF são usados como identificadores de solicitação.

Se um aplicativo receber um erro retornando que ele não trata especificamente (como um erro definido por uma extensão específica do dispositivo), ele deve tratar o erro como um LINEERR \_ OPERATIONFAILED (por um motivo não especificado).

Ao invocar as \_ constantes LINEERR que são novas com a TAPI 3,0, o arquivo Tapierr.MC deve ser atualizado com novas mensagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)
</dt> <dt>

[**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




