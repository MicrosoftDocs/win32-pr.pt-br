---
description: A \_ mensagem de LINEDEVSTATE de linha TAPI é enviada quando o estado de um dispositivo de linha é alterado. O aplicativo pode invocar lineGetLineDevStatus para determinar o novo status da linha.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Mensagem de LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261e7527354b84801437e48ffc13ba4dbad60ced0cca61be65eb96ce6417bb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682377"
---
# <a name="line_linedevstate-message"></a>Mensagem de LINEDEVSTATE de linha \_

A mensagem **de \_ LINEDEVSTATE de linha** TAPI é enviada quando o estado de um dispositivo de linha é alterado. O aplicativo pode invocar [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) para determinar o novo status da linha.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para o dispositivo de linha. Esse parâmetro é **nulo** quando *dwParam1* é LINEDEVSTATE \_ reinit.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha. Se o parâmetro *dwParam1* for LINEDEVSTATE \_ REINIT, o parâmetro *dwCallBackInstance* não será válido e será definido como zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O item de status do dispositivo de linha que foi alterado. O parâmetro pode ser uma ou mais das [**\_ constantes LINEDEVSTATE**](linedevstate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

A interpretação desse parâmetro depende do valor de *dwParam1*. Se *dwParam1* for LINEDEVSTATE \_ tocando, *dwParam2* conterá o modo de anel com o qual a opção instrui a linha a tocar. Os modos de toque válidos são números no intervalo um para **dwNumRingModes**, em que **dwNumRingModes** é uma funcionalidade de dispositivo de linha.

Se *dwParam1* for LINEDEVSTATE \_ reinit e a mensagem tiver sido emitida pela TAPI como resultado da conversão de uma nova mensagem de API em uma mensagem de reinicialização, *dwParam2* conterá o parâmetro *dwMsg* da mensagem original (por exemplo, [**linha \_ Create**](line-create.md) ou line \_ LINEDEVSTATE). Se *dwParam2* for zero, isso indica que a mensagem de reinicialização é uma mensagem de reinicialização "real" que exige que o aplicativo chame [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) de sua primeira conveniência.

</dd> <dt>

*dwParam3* 
</dt> <dd>

A interpretação desse parâmetro depende do valor de *dwParam1*. Se *dwParam1* for LINEDEVSTATE \_ tocando, *dwParam3* conterá a contagem de anéis para este evento de toque. A contagem de anéis começa em zero.

Se *dwParam1* for LINEDEVSTATE \_ reinit e a mensagem tiver sido emitida pela TAPI como resultado da conversão de uma nova mensagem de API em uma mensagem de reinicialização, *dwParam3* conterá o parâmetro *dwParam1* da mensagem original (por exemplo, LINEDEVSTATE \_ TRANSLATECHANGE ou algum outro \_ valor LINEDEVSTATE, se *dwParam2* for line \_ LINEDEVSTATE ou o novo identificador de dispositivo, se *dwParam2* for [**line \_ Create**](line-create.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O envio da mensagem **\_ LINEDEVSTATE de linha** pode ser controlado com [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Um aplicativo pode indicar alterações de item de status sobre as quais deseja ser notificado. Por padrão, todos os relatórios de status são desabilitados, exceto para \_ REinicialização de LINEDEVSTATE, que não pode ser desabilitado. Essa mensagem é enviada para todos os aplicativos que têm um identificador para a linha, incluindo aqueles que chamaram [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) com o parâmetro *DWPRIVILEGES* definido como LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ Monitor ou as combinações permitidas desses.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**fechamento de linha \_**](line-close.md)
</dt> <dt>

[**criação de linha \_**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




