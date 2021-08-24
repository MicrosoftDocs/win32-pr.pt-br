---
description: ICE86 emite um aviso se o pacote usa a propriedade AdminUser na coluna de banco de dados do tipo Condition. Os autores de pacote devem usar a propriedade Privileged em instruções condicionais.
ms.assetid: c23c2920-3b8b-4cd1-a570-bdeabcf11436
title: ICE86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c96e572a99fc31fea540fa4fbaad4179d1e8f2ecadebfcd9222527ca6a4afac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894986"
---
# <a name="ice86"></a>ICE86

ICE86 emite um aviso se o pacote usa a [**propriedade AdminUser**](adminuser.md) na coluna de banco de dados do [tipo](condition.md) Condition. Os autores de pacote devem usar [**a propriedade Privileged**](privileged.md) em instruções condicionais.

## <a name="result"></a>Resultado

ICE86 posta o aviso a seguir.



| Aviso ICE86                                                                                               | Descrição                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Propriedade \` %s \` encontrada na coluna \` \` %s. \` %s \` na linha %s. \`A \` propriedade privileged geralmente é mais apropriada. | [**A propriedade AdminUser**](adminuser.md) foi usada em um campo Condição. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



