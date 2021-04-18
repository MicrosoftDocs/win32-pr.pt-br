---
description: As \_ constantes de sinalizador de bit LINEDEVCAPFLAGS são uma coleção de boolianos que descreve vários recursos de dispositivo de linha.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Constantes de LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766973"
---
# <a name="linedevcapflags_-constants"></a>\_Constantes LINEDEVCAPFLAGS

As constantes de sinalizador de bit **LINEDEVCAPFLAGS \_** são uma coleção de boolianos que descreve vários recursos de dispositivo de linha.

<dl> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS \_ CALLHUB**
</dt> <dd> <dl> <dt>



Indica se os hubs de chamada têm suporte nesta linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Indica se o acompanhamento do hub de chamadas tem suporte nesta linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS \_ CLOSEDROP**
</dt> <dd> <dl> <dt>



Especifica o que acontece quando uma linha aberta é fechada enquanto o aplicativo chama ativo na linha. Se **for true**, o provedor de Serviços descartará (limpará) todas as chamadas ativas na linha quando o último aplicativo que abriu a linha a fechar com [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose). Se **for false**, o provedor de serviços não descartará chamadas ativas nesses casos. Em vez disso, as chamadas permanecem ativas e sob o controle de dispositivos externos. Um provedor de serviços normalmente define esse bit como **false** se houver algum outro dispositivo que possa manter a chamada ativa, por exemplo, se uma linha analógica tiver o computador e o conjunto de telefone se conectar diretamente a eles em uma configuração de linha de terceiros, o telefone offhook manterá automaticamente a chamada ativa mesmo depois que o computador for desligado.

Os aplicativos devem verificar esse sinalizador para determinar se deve avisar o usuário (com uma caixa de diálogo OK/cancelar) de que as chamadas ativas serão perdidas.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS \_ CROSSADDRCONF**
</dt> <dd> <dl> <dt>



Especifica se as chamadas em endereços diferentes nessa linha podem ser conferências.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS \_ DIALBILLING**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS \_ DIALDIALTONE**
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS \_ DIALQUIET**
</dt> <dd> <dl> <dt>



Esses sinalizadores indicam se o modificador de cadeia de caracteres de discagem "$", "@" ou "W" tem suporte para um determinado dispositivo de linha. Será **verdadeiro** se o modificador for suportado; caso contrário, **false**. O "?" (avisar o usuário para continuar a discagem) nunca é suportado por um dispositivo de linha. Esses sinalizadores permitem que um aplicativo determine antecipadamente quais modificadores resultariam na geração de um LINEERR. O aplicativo tem a opção de cadeias de caracteres de discagem antes da verificação para não há suporte ou para a transmissão da cadeia de caracteres "RAW" de [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) diretamente para o provedor como parte de funções como [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) ou [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e permite que a função gere um erro para informar qual modificador sem suporte ocorre primeiro na cadeia de caracteres.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS \_ HIGHLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica se os elementos de informações de compatibilidade de alto nível têm suporte nesta linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS \_ LOWLEVCOMP**
</dt> <dd> <dl> <dt>



Especifica se os elementos de informações de compatibilidade de nível baixo têm suporte nesta linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS \_ MEDIACONTROL**
</dt> <dd> <dl> <dt>



Especifica se as operações de controle de mídia estão disponíveis para chamadas nesta linha.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS \_ MSP**
</dt> <dd> <dl> <dt>



Indica se um MSP (provedor de serviços de mídia) está associado à linha. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS \_ MULTIPLEADDR**
</dt> <dd> <dl> <dt>



Especifica se [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ou [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) é capaz de lidar com vários endereços de uma vez (como para multiplexação inversa).


</dt> </dl> </dd> <dt>

<span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS \_ PRIVATEOBJECTS**
</dt> <dd> <dl> <dt>



Indica se as [interfaces específicas do provedor](./provider-specific-interfaces.md) foram implementadas. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.


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

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

