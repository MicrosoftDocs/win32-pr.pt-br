---
description: As \_ constantes de sinalizador de bit PHONEPRIVILEGE descrevem as várias maneiras em que um dispositivo de telefone pode ser aberto.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Constantes de PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760149"
---
# <a name="phoneprivilege_-constants"></a>\_Constantes PHONEPRIVILEGE

As constantes de sinalizador de bit **PHONEPRIVILEGE \_** descrevem as várias maneiras em que um dispositivo de telefone pode ser aberto.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**MONITOR de PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Um aplicativo que abre um dispositivo de telefone com o privilégio de monitor é informado sobre eventos e alterações de estado que ocorrem no telefone. O aplicativo não pode invocar nenhuma operação no dispositivo de telefone que alteraria seu estado, portanto, somente as operações de status podem ser invocadas. Vários aplicativos podem monitorar um dispositivo de telefone em um determinado momento.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**proprietário do PHONEPRIVILEGE \_**
</dt> <dd> <dl> <dt>



Um aplicativo que abre um dispositivo de telefone com o privilégio de proprietário tem permissão para alterar o estado das lâmpadas, do toque, da exibição, da Hookswitch e dos blocos de dados do telefone. Abrir um dispositivo de telefone no modo de proprietário também fornece o monitoramento do dispositivo de telefone. Somente um aplicativo pode ser o proprietário de um dispositivo de telefone em um determinado momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




