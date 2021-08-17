---
description: ICE97 verifica se dois componentes não isolam um componente compartilhado no mesmo diretório.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29575d533e945cef922110315cd3300f56fe62ae61b34c92de7175916e6657ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315236"
---
# <a name="ice97"></a>ICE97

ICE97 verifica se dois componentes não isolam um componente compartilhado no mesmo diretório.

## <a name="result"></a>Resultado

ICE97 posta os avisos a seguir.



| Aviso ICE97                                                                                                                                                                    | Descrição                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Esse componente 1 instala o componente Compartilhado no mesmo diretório 2 que outro, o que interrompe as regras de componente se os \[ \] componentes (ou mais) estão selecionados \[ \] para instalação. | Dois componentes não devem isolar um componente compartilhado no mesmo diretório. |



 

Por exemplo, Component1 e Component2, que compartilham ComponentShared, são instalados no mesmo diretório. Ambos especificam ComponentShared como um componente isolado. Devido ao isolamento, os arquivos em ComponentShared são copiados duas vezes para a referência de Diretório \_ para Component1 e Component2. Os componentes agora têm uma contagem de referência na cópia de arquivos. Isso está violando as regras de componente do Instalador. Se Component1 for desinstalado, os arquivos de componentes isolados serão removidos e Component2 será desfeito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



