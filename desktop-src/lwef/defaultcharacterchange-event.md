---
title: Evento DefaultCharacterChange
description: Evento DefaultCharacterChange
ms.assetid: 14b86a44-8fd2-4719-b7b5-cdcc618d27cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed166608d3f3b874e975ff58f600d24b73b50e293333b841039b2240780b4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963126"
---
# <a name="defaultcharacterchange-event"></a>Evento DefaultCharacterChange

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário altera o caractere padrão.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Sub** *Agent. * * * DefaultCharacterChange* *  **(ByVal** *GUID * * *)**



| Parte   | Descrição                                      |
|--------|--------------------------------------------------|
| *GUID* | Retorna o identificador exclusivo do caractere. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Esse evento indica quando o usuário alterou o caractere atribuído como o caractere padrão do usuário. O servidor envia isso somente para clientes que carregaram o caractere padrão.

Quando o novo caractere é exibido, ele assume o mesmo tamanho que qualquer instância já carregada do caractere ou o caractere padrão anterior (nessa ordem).

### <a name="see-also"></a>Consulte Também

[**Método ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md), [ **método Load**](load-method.md)


 

 




