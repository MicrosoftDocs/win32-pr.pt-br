---
description: As constantes de sinalizador de bits LINEDEVCAPFLAGS são uma \_ coleção de boolianas que descrevem vários recursos de dispositivo de linha.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: LINEDEVCAPFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d54acf1855bc09d9b2160e1ae681b25ff1de8ce310049fd4aabf4af6f8f2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761713"
---
# <a name="linedevcapflags_-constants"></a>Constantes LINEDEVCAPFLAGS \_

As constantes de sinalizador de bits **LINEDEVCAPFLAGS \_** são uma coleção de boolianas que descrevem vários recursos de dispositivo de linha.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indica se há suporte para hubs de chamada nessa linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão TAPI 3.0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indica se há suporte para o acompanhamento do hub de chamada nessa linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão TAPI 3.0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Especifica o que acontece quando uma linha aberta é fechada enquanto o aplicativo tem chamadas ativas na linha. Se **TRUE**, o provedor de serviços descarta (limpa) todas as chamadas ativas na linha quando o último aplicativo que abriu a linha o fecha com [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Se **FOR FALSE,** o provedor de serviços não soltará chamadas ativas nesses casos. Em vez disso, as chamadas permanecem ativas e sob controle de dispositivos externos. Um provedor de serviços normalmente define esse bit como **FALSE** se houver algum outro dispositivo que possa manter a chamada ativa, por exemplo, se uma linha análoga tiver o computador e o telefone definidos para se conectarem diretamente a eles em uma configuração de linha de parte, o telefone de offhook manterá automaticamente a chamada ativa mesmo depois que o computador desligar.

Os aplicativos devem verificar esse sinalizador para determinar se devem avisar o usuário (com uma caixa de diálogo OK/Cancelar) de que as chamadas ativas serão perdidas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Especifica se chamadas em endereços diferentes nessa linha podem ser conferênciadas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Esses sinalizadores indicam se o modificador de cadeia de caracteres discável "$", "@" ou "W" tem suporte para um determinado dispositivo de linha. Será **TRUE se** o modificador tiver suporte; caso contrário, **FALSE.** O "?" (solicitar que o usuário continue discando) nunca é suportado por um dispositivo de linha. Esses sinalizadores permitem que um aplicativo determine na frente quais modificadores resultariam na geração de um LINEERR. O aplicativo tem a opção de pré-verificação de cadeias de caracteres discáveis para caracteres sem suporte ou de passar a cadeia de caracteres "bruta" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) diretamente para o provedor como parte de funções como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e permitir que a função gere um erro para dizer qual modificador sem suporte ocorre primeiro na cadeia de caracteres.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica se há suporte para elementos de informações de compatibilidade de alto nível nessa linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica se há suporte para elementos de informações de compatibilidade de baixo nível nessa linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Especifica se as operações de controle de mídia estão disponíveis para chamadas nesta linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Indica se um MSP (Provedor de Serviços de Mídia) está associado à linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão TAPI 3.0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Especifica se [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial,**](/windows/desktop/api/Tapi/nf-tapi-linedial) [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ou [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) é capaz de lidar com vários endereços de uma vez (quanto à multiplexação inversa).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Indica se interfaces [específicas do provedor](./provider-specific-interfaces.md) foram implementadas. Esse sinalizador é exposto somente a aplicativos que negociam uma versão TAPI 3.0 ou superior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**Linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**Linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**Linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

