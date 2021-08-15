---
description: As constantes de sinalizador de bits PHONEPRIVILEGE descrevem as várias maneiras pelas quais um dispositivo \_ de telefone pode ser aberto.
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: PHONEPRIVILEGE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9b3f3848af8c9858522bd924ccb77d7bf1682f09b66c0cfdcb5527b93416dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761288"
---
# <a name="phoneprivilege_-constants"></a>Constantes PHONEPRIVILEGE \_

As constantes de sinalizador de bits **PHONEPRIVILEGE \_** descrevem as várias maneiras pelas quais um dispositivo de telefone pode ser aberto.

<dl> <dt>

<span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE \_ MONITOR**
</dt> <dd> <dl> <dt>



Um aplicativo que abre um dispositivo de telefone com o privilégio de monitor é informado sobre eventos e alterações de estado que ocorrem no telefone. O aplicativo não pode invocar nenhuma operação no dispositivo de telefone que alteraria seu estado, portanto, somente as operações de status podem ser invocadas. Vários aplicativos podem monitorar um dispositivo de telefone a qualquer momento.


</dt> </dl> </dd> <dt>

<span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE \_ OWNER**
</dt> <dd> <dl> <dt>



Um aplicativo que abre um dispositivo de telefone com o privilégio de proprietário tem permissão para alterar o estado das lâmpadas, anéis, exibição, ganchos e blocos de dados do telefone. Abrir um dispositivo de telefone no modo de proprietário também fornece monitoramento do dispositivo de telefone. Somente um aplicativo tem permissão para ser o proprietário de um dispositivo de telefone em um determinado momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




