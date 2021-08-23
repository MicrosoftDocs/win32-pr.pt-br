---
title: Propriedade Page
description: Propriedade Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ca14a4f68c326d1b231aa106450fefc7607857576f817ffaa255fa27f2249b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601005"
---
# <a name="page-property"></a>Propriedade Page

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a página exibida na janela de folha de propriedades do Microsoft Agent.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. PropertySheet.Page* cadeia de *  \[  =  *caracteres*\]



| Parte     | Descrição                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres com um dos valores a seguir. **"Fala"** Exibe a página Entrada de Fala.<br/> **"Saída"** Exibe a página Saída.<br/> **"Copyright"** Exibe a página Direitos Autorais.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se nenhum mecanismo de fala estiver instalado, a **definição de Página** **como "Fala"** não terá nenhum efeito. Além disso, a propriedade **Visible** da janela deve ser definida como **True** para que o usuário veja a página.

> [!Note]  
> O usuário pode substituir essa propriedade.

 

 

 





