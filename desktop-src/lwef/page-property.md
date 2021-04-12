---
title: Propriedade Page
description: Propriedade Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363982"
---
# <a name="page-property"></a>Propriedade Page

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a página exibida na janela da folha de propriedades do Microsoft Agent.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agent * * *.* *  \[  =  *Cadeia de caracteres* PropertySheet.Page\]



| Parte     | Descrição                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres com um dos valores a seguir. **"Fala"** Exibe a página de entrada de fala.<br/> **"Saída"** Exibe a página saída.<br/> **"Direitos autorais"** Exibe a página de direitos autorais.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se nenhum mecanismo de fala estiver instalado, a configuração **da página** como **"fala"** não terá efeito. Além disso, a propriedade **Visible** da janela deve ser definida como **true** para que o usuário veja a página.

> [!Note]  
> O usuário pode substituir essa propriedade.

 

 

 





