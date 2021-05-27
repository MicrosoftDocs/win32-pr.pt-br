---
title: Falha de desenho D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Falha em uma chamada draw por um destino de renderização
keywords:
- D1109 Falha de desenho Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549961"
---
# <a name="d1109-draw-failure"></a>D1109: Falha de desenho

Uma chamada draw por um recurso de destino de \[ *renderização com falha.* \] Marcas \[ *tag1*, *tag2* \] .

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recurso*
</dt> <dd>

O endereço do destino de renderização.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

O primeiro valor da marca (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

O segundo valor da marca (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) mais para obter informações).

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="possible-causes"></a>Possíveis causas

Há muitos motivos pelos quais uma chamada draw pode falhar. Para obter mais informações, consulte a documentação do SDK do Direct2D para o método que falhou.

 

 