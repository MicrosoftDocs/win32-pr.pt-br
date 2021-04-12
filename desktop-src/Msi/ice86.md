---
description: ICE86 emitirá um aviso se o pacote usar a propriedade AdminUser na coluna de banco de dados do tipo de condição. Os autores de pacote devem usar a propriedade Privileged em instruções condicionais.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25df1e2a9c3ab610e78efd6f797cb916f0563e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297203"
---
# <a name="ice86"></a>ICE86

ICE86 emitirá um aviso se o pacote usar a propriedade [**AdminUser**](adminuser.md) na coluna de banco de dados do tipo de [condição](condition.md) . Os autores de pacote devem usar a propriedade [**Privileged**](privileged.md) em instruções condicionais.

## <a name="result"></a>Resultado

ICE86 posta o aviso a seguir.



| Aviso de ICE86                                                                                               | Descrição                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Propriedade \` % s \` encontrada na coluna \` % s \` . \` % s \` na linha% s. \`A \` Propriedade privilegiada é geralmente mais apropriada. | A propriedade [**AdminUser**](adminuser.md) foi usada em um campo de condição. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



