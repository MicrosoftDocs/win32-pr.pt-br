---
description: As \_ constantes LINETONEMODE descrevem seleções diferentes que são usadas ao gerar tons de linha.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Constantes de LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759963"
---
# <a name="linetonemode_-constants"></a>\_Constantes LINETONEMODE

As **\_ constantes LINETONEMODE** descrevem seleções diferentes que são usadas ao gerar tons de linha.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_aviso sonoro de LINETONEMODE**
</dt> <dd> <dl> <dt>



O Tom é um aviso sonoro, como aquele usado para anunciar o início de uma gravação. A definição exata é um provedor de serviços definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**cobrança do LINETONEMODE \_**
</dt> <dd> <dl> <dt>



O Tom é um tom de informações de cobrança, como um tom de pedido de cartão de crédito. A definição exata é um provedor de serviços definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ ocupado**
</dt> <dd> <dl> <dt>



O Tom é um tom ocupado. A definição exata é um provedor de serviços definido.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizado**
</dt> <dd> <dl> <dt>



O Tom é um tom personalizado definido por suas frequências de componente, do tipo [**lineGenerateTone**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE de \_ toque**
</dt> <dd> <dl> <dt>



O Tom é Tom de toque. A definição exata é um provedor de serviços definido.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo. Os 16 bits de ordem inferior são reservados.

Essas constantes são usadas para definir tons a serem gerados na faixa em uma chamada para a parte remota. Observe que a detecção de Tom de tons não personalizados não usa essas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




