---
title: Método ShowDefaultCharacterProperties
description: Método ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d19f92f555038fe4c13c7a752d49bf35a04b70964f6110d881976af3e72a8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746302"
---
# <a name="showdefaultcharacterproperties-method"></a>Método ShowDefaultCharacterProperties

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Exibe as propriedades do caractere padrão.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. ShowDefaultCharacterProperties* *  \[ *X,* *Y*\]



| Parte | Descrição                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Opcional. Um valor inteiro curto que indica a coordenada de tela horizontal (*X* ) para exibir a janela. Essa coordenada deve ser especificada em pixels. |
| *S*  | Opcional. Um valor inteiro curto que indica a coordenada de tela vertical (*Y*) para exibir a janela. Essa coordenada deve ser especificada em pixels.    |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Chamar esse método exibe a janela de propriedades de caractere padrão (não a folha de propriedades do Microsoft Agent). Se você não especificar as coordenadas X e Y, a janela aparecerá no último local em que foi exibida.

## <a name="see-also"></a>Consulte Também

[**Evento DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




