---
description: O ICE11 é usado com instalações simultâneas. As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte instalações simultâneas.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922022"
---
# <a name="ice11"></a>ICE11

O ICE11 é usado com instalações simultâneas. As instalações simultâneas não são recomendadas para a instalação de aplicativos destinados ao lançamento para o público. Para obter informações sobre instalações simultâneas, consulte [instalações simultâneas](concurrent-installations.md).

## <a name="result"></a>Resultado

ICE11 valida a coluna de origem da [tabela CustomAction](customaction-table.md) de ações personalizadas de instalação simultânea. A coluna de origem deve conter um [GUID](guid.md) (código de produto msi) válido.

ICE11 posta um erro se a coluna de origem da tabela CustomAction é criada incorretamente para ações personalizadas de instalação simultânea.

## <a name="example"></a>Exemplo

ICE posta as seguintes mensagens de erro para o exemplo mostrado.

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

[Tabela de propriedades](property-table.md) (parcial)



| Propriedade        | Valor                                  |
|-----------------|----------------------------------------|
| **ProductCode** | {BFB69273-F0AE-45C4-9853-0AF946714768} |



 

[Tabela CustomAction](customaction-table.md) (parcial)



| CustomAction | Tipo | Fonte                                 |
|--------------|------|----------------------------------------|
| CA1          | 39   | {BFB69273-F0AE-45C4-9853-0AF946714768} |
| CA2          | 39   | {BFB69273-F0AE-55c5-9853-0AF946714768} |
| CA3          | 39   | {BFB69273-F0AE-66C6-9853-0AF946714768} |
| CA4          | 39   | ProductCode                            |



 

Para corrigir os erros, para CA1, você não pode fazer uma instalação simultânea do "pacote base". Isso resultaria em uma instalação recursiva. Essa entrada deve ser removida ou a coluna de origem deve ser alterada para um GUID de um MSI anunciado que seja diferente do GUID do pacote base. Para CA2, torne todos os caracteres do GUID de maiúsculas. Por fim, altere a coluna de origem CA4's para fazer referência a um GUID válido de um MSI anunciado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalações simultâneas](concurrent-installations.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



