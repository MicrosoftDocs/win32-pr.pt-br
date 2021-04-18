---
description: As \_ constantes LINEOPENOPTION listam as opções disponíveis para abrir uma linha.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes de LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779453"
---
# <a name="lineopenoption_-constants"></a>\_Constantes LINEOPENOPTION

As **\_ constantes LINEOPENOPTION** listam as opções disponíveis para abrir uma linha.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**
</dt> <dd> <dl> <dt>



O aplicativo está disposto a lidar com solicitações de outros aplicativos que têm a linha aberta.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



O aplicativo deve ser informado sobre novas chamadas criadas no dispositivo de linha somente se essas chamadas aparecerem no endereço especificado no membro **dwAddressID** na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) apontada pelo parâmetro *lpCallParams* .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Consulte [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) para obter mais detalhes sobre a operação dessas opções.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




