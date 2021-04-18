---
description: As \_ constantes de sinalizador de bit LINETRANSFERMODE descrevem diferentes maneiras de resolver solicitações de transferência de chamada.
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Constantes de LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781037"
---
# <a name="linetransfermode_-constants"></a>\_Constantes LINETRANSFERMODE

As constantes de sinalizador de bit **LINETRANSFERMODE \_** descrevem diferentes maneiras de resolver solicitações de transferência de chamada.

<dl> <dt>

<span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_conferência LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



A transferência é resolvida estabelecendo uma conferência de três vias entre o aplicativo, a parte conectada à chamada inicial e a parte conectada à chamada de consulta. Uma chamada de conferência é criada quando essa opção é selecionada.


</dt> </dl> </dd> <dt>

<span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_transferência LINETRANSFERMODE**
</dt> <dd> <dl> <dt>



A transferência é resolvida transferindo a chamada inicial para a chamada de consulta. Ambas as chamadas ficarão ociosas para o aplicativo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




