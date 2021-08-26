---
title: Propriedade ForeColor
description: Propriedade ForeColor
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebfc7f0b64a43f7ccb9075426a75df9a777fbb8b1e5e94cb16e747e0681cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962755"
---
# <a name="forecolor-property"></a>Propriedade ForeColor

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna a cor de primeiro plano exibida atualmente na janela de balão do texto para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente ***. Caracteres ("**_characterid_*_"). Balloon. ForeColor_*

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **ForeColor** retorna um valor que especifica a cor do texto na palavra balão. O intervalo válido para uma cor RGB normal é de 0 a 16.777.215 (&HFFFFFF). O byte alto de um número neste intervalo é igual a 0; os 3 bytes inferiores, do menos ao byte mais significativo, determinam a quantidade de vermelho, verde e azul, respectivamente. Cada um dos componentes vermelho, verde e azul é representado por um número entre 0 e 255 (&HFF).

 

 




