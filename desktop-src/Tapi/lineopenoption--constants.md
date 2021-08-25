---
description: As constantes LINEOPENOPTION \_ listam as opções disponíveis para abrir uma linha.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: LINEOPENOPTION_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739246"
---
# <a name="lineopenoption_-constants"></a>Constantes LINEOPENOPTION \_

As **\_ constantes LINEOPENOPTION** listam as opções disponíveis para abrir uma linha.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION \_ PROXY**
</dt> <dd> <dl> <dt>



O aplicativo está disposto a lidar com solicitações de outros aplicativos que têm a linha aberta.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



O aplicativo deverá ser informado sobre novas chamadas criadas no dispositivo de linha somente se essas chamadas aparecerem no endereço especificado no membro **dwAddressID** na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) apontada pelo parâmetro *lpCallParams.*


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Consulte [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obter mais detalhes sobre a operação dessas opções.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




