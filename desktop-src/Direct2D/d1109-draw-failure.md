---
title: Falha de desenho D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Uma chamada de empate por um destino de renderização falhou
keywords:
- Direct2D de falha de desenho D1109
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b1d30d0b33cbeb053e37f9e52c3948009a19692dbe1c53eedab9dfd6623726a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814786"
---
# <a name="d1109-draw-failure"></a>D1109: falha ao desenhar

Uma chamada de empate por um recurso com falha de destino de renderização \[  \] . Marcas \[ *da tag1*, *tag2* \] .

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Kit*
</dt> <dd>

O endereço do destino de renderização.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*da tag1*
</dt> <dd>

O primeiro valor de marca (consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter informações).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

O segundo valor de marca (consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="possible-causes"></a>Possíveis causas

Há muitas razões pelas quais uma chamada de empate pode falhar. para obter mais informações, consulte a documentação do SDK do Direct2D para o método que falhou.

 

 