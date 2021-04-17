---
description: Esta é a lista de códigos de erro que a implementação pode retornar ao invocar operações em dispositivos de telefone. Consulte as descrições de função individuais para determinar quais desses códigos de erro cada função pode retornar.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Constantes de PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756989"
---
# <a name="phoneerr_-constants"></a>\_Constantes PHONEERR

Esta é a lista de códigos de erro que a implementação pode retornar ao invocar operações em dispositivos de telefone. Consulte as descrições de função individuais para determinar quais desses códigos de erro cada função pode retornar.

<dl> <dt>

<span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ alocada**
</dt> <dd> <dl> <dt>



O recurso especificado já está alocado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



O identificador de dispositivo especificado é inválido ou está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ desconectado**
</dt> <dd> <dl> <dt>



A chamada foi desconectada.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



O aplicativo solicitou uma versão de API ou um intervalo de versão que não pode ser suportado pela implementação da API de telefonia ou pelo provedor de serviços correspondente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



O aplicativo solicitou uma versão de extensão ou um intervalo de versão que não pode ser suportado pelo provedor de serviços.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



Devido a inconsistências internas ou problemas de formatação no arquivo Telephon.ini, ele não pode ser lido e compreendido corretamente pela TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ INUSE**
</dt> <dd> <dl> <dt>



O dispositivo está em uso no momento. O dispositivo não pode ser configurado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



O identificador de uso ou o identificador de registro especificado do aplicativo é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



O nome do aplicativo especificado é inválido. Se um nome de aplicativo for especificado pelo aplicativo, supõe-se que a cadeia de caracteres não contém nenhum caractere que não seja exibido e é terminada em **nulo**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**
</dt> <dd> <dl> <dt>



O identificador de botão/lâmpada especificado está fora do intervalo ou é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modo de botão é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**
</dt> <dd> <dl> <dt>



O parâmetro de Estados de botão é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**
</dt> <dd> <dl> <dt>



O identificador de dados especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



O telefone especificado não oferece suporte à classe de dispositivo indicada.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



O número de versão da extensão do provedor de serviços é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



O parâmetro do Dispositivo Hookswitch é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modo Hookswitch é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modo de lâmpada especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Um parâmetro, como um valor de linha ou coluna ou um identificador de janela, é inválido ou está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**
</dt> <dd> <dl> <dt>



O identificador do dispositivo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**
</dt> <dd> <dl> <dt>



O dispositivo de telefone não está em um estado válido para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Um ou mais dos parâmetros de ponteiro especificados são inválidos.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**
</dt> <dd> <dl> <dt>



O parâmetro *dwPrivilege* é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**
</dt> <dd> <dl> <dt>



O parâmetro de modo de anel é inválido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



O identificador de dispositivo especificado, que era válido anteriormente, não é mais aceito porque o dispositivo associado foi removido do sistema desde que a TAPI foi inicializada pela última vez ou está corrompido de uma forma que não foi detectada na inicialização.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOunidade**
</dt> <dd> <dl> <dt>



O provedor de serviços de telefonia para o dispositivo especificado descobriu que um de seus componentes está ausente ou corrompido de uma maneira que não foi detectada no momento da inicialização. O usuário deve ser aconselhado a usar o painel de controle de telefonia para corrigir o problema.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**nome do PHONEERR \_**
</dt> <dd> <dl> <dt>



Memória insuficiente para concluir a operação solicitada ou não é possível alocar ou bloquear memória.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_ NOcidade**
</dt> <dd> <dl> <dt>



O aplicativo não tem o privilégio de proprietário para o dispositivo de telefone especificado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**
</dt> <dd> <dl> <dt>



A operação falhou por um motivo não especificado.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**
</dt> <dd> <dl> <dt>



A operação não está disponível.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**reinicialização do PHONEERR \_**
</dt> <dd> <dl> <dt>



Se a reinicialização da TAPI tiver sido solicitada, por exemplo, como resultado da adição ou remoção de um provedor de serviços de telefonia, as solicitações [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) ou [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) serão rejeitadas com esse erro até que o último aplicativo encerre seu uso da API (usando [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), quando a nova configuração entrar em vigor e os aplicativos forem novamente permitidos para chamar **phoneInitialize** ou **phoneInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



O número máximo de solicitações de telefone pendentes foi excedido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**
</dt> <dd> <dl> <dt>



A operação não pode ser concluída devido a um sobrecompromisso de recurso.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**
</dt> <dd> <dl> <dt>



A estrutura de Caps telefônicas especificada é muito pequena.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR não \_ inicializado**
</dt> <dd> <dl> <dt>



A operação foi invocada antes de qualquer aplicativo chamado [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os valores de 0xC0000000 a 0xFFFFFFFF estão disponíveis para extensões específicas do dispositivo; os valores 0x80000000 a 0xBFFFFFFF são reservados; e 0x00000000 a 0x7FFFFFFF são usados como identificadores de solicitação.

Se um aplicativo receber um erro retornando que ele não trata especificamente (como um erro definido por uma extensão específica do dispositivo), ele deve tratar o erro como um PHONEERR \_ OPERATIONFAILED (por um motivo não especificado).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




