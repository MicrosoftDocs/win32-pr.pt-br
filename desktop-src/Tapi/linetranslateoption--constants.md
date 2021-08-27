---
description: A \_ constante de sinalizador de bit LINETRANSLATEOPTION descreve uma opção usada pela conversão de endereços.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Constantes de LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d1cc9f3d7798dda9dd5bb69817ccfac64ae88fbc45fccccd59563cc24614d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073016"
---
# <a name="linetranslateoption_-constants"></a>\_Constantes LINETRANSLATEOPTION

A constante de sinalizador de bit **LINETRANSLATEOPTION \_** descreve uma opção usada pela conversão de endereços.

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



Se uma cadeia de caracteres de espera de chamada de cancelamento for definida para o local, definir esse bit fará com que essa cadeia de caracteres seja inserida no início da cadeia de caracteres de discagem. Isso é comumente usado por aplicativos de fax e de modem de dados para evitar a interrupção de chamadas por alarmes de espera de chamada. Se nenhuma cadeia de caracteres de espera de chamada de cancelamento for definida para o local, esse bit não terá nenhum efeito. Observe que os aplicativos que usam esse bit também são aconselhados a definir o \_ bit seguro LINECALLPARAMFLAGS no membro **dwCallParamFlags** da estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passada para [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) por meio do parâmetro *lpCallParams* , de forma que, se o dispositivo de linha usar um mecanismo diferente de dígitos de discagem para suprimir as interrupções de chamada, esse mecanismo será invocado.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



O cartão de chamada padrão deve ser substituído por um especificado.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



Essa opção força o endereço (número) a ser convertido como longa distância.


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



Essa opção força o número (endereço) a ser traduzido como local.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




