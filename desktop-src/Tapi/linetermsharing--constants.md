---
description: As \_ constantes de sinalizador de bit LINETERMSHARING descrevem diferentes maneiras em que um terminal pode ser compartilhado entre dispositivos de linha, endereços ou chamadas.
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: Constantes de LINETERMSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760334"
---
# <a name="linetermsharing_-constants"></a>\_Constantes LINETERMSHARING

As constantes de sinalizador de bit **LINETERMSHARING \_** descrevem diferentes maneiras em que um terminal pode ser compartilhado entre dispositivos de linha, endereços ou chamadas.

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ privado**
</dt> <dd> <dl> <dt>



O dispositivo de terminal é privado para um dispositivo de linha única.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**
</dt> <dd> <dl> <dt>



O dispositivo de terminal pode ser usado por várias linhas. As solicitações de [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) dos vários terminais acabam sendo mescladas ou enconferênciadas no terminal.


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**
</dt> <dd> <dl> <dt>



O dispositivo de terminal pode ser usado por várias linhas. O último dispositivo de linha para fazer um [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) ou [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) para o terminal para um determinado modo de terminal terá uma conexão exclusiva com o terminal para esse modo.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

Essas constantes descrevem as classes de fluxo de controle e de informações que podem ser roteadas diretamente entre um dispositivo de linha e um dispositivo de terminal (como um conjunto de telefone).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

