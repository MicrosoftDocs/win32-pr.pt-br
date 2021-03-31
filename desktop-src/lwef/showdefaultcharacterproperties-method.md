---
title: Método ShowDefaultCharacterProperties
description: Método ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635706"
---
# <a name="showdefaultcharacterproperties-method"></a>Método ShowDefaultCharacterProperties

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Exibe as propriedades do caractere padrão.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent * * *. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Parte | Descrição                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Opcional. Um valor inteiro curto que indica a coordenada de tela horizontal (*X* ) para exibir a janela. Essa coordenada deve ser especificada em pixels. |
| *S*  | Opcional. Um valor inteiro curto que indica a coordenada de tela vertical (*Y*) para exibir a janela. Essa coordenada deve ser especificada em pixels.    |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Chamar esse método exibe a janela Propriedades de caractere padrão (não a folha de propriedades do Microsoft Agent). Se você não especificar as coordenadas X e Y, a janela será exibida no último local em que foi exibida.

## <a name="see-also"></a>Consulte Também

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




