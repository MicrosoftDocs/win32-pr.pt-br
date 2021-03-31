---
title: Restrições na extensão do esquema
description: Para reduzir a possibilidade de alterações de esquema em um aplicativo que está interrompendo outros aplicativos e manter a consistência do esquema, Active Directory Domain Services impor restrições sobre o tipo de alterações de esquema que um aplicativo ou usuário tem permissão para fazer.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634924"
---
# <a name="restrictions-on-schema-extension"></a>Restrições na extensão do esquema

Para reduzir a possibilidade de alterações de esquema em um aplicativo que está interrompendo outros aplicativos e manter a consistência do esquema, Active Directory Domain Services impor restrições sobre o tipo de alterações de esquema que um aplicativo ou usuário tem permissão para fazer.

As restrições são impostas apenas na modificação de objetos de esquema existentes. O esquema é categorizado em duas categorias. Os objetos de esquema que acompanham o Windows 2000 no esquema base pertencem à categoria 1. Todos os objetos de esquema adicionados posteriormente por outros aplicativos ou usuários por meio da extensão de esquema dinâmico pertencem à categoria 2. A categoria de um objeto de esquema pode ser determinada pelo conjunto de bits 0x10 definido no atributo **systemFlags** no objeto **classSchema** . Esse bit só é definido na categoria 1 objetos e não pode ser alterado, nem pode ser definido em qualquer objeto Category 2.

O atributo **systemFlags** é usado internamente pelo Active Directory Domain Services para identificar características especiais de objetos de "infraestrutura" no esquema de base. Além de identificar objetos da categoria 1, **systemFlags** controla se um objeto pode ser movido, excluído ou renomeado. Essas operações são impedidas para objetos que o Windows 2000 depende para serem executados.

Em qualquer objeto de esquema, categoria 1 ou 2, Active Directory Domain Services impor as seguintes restrições:

-   Você não pode adicionar um novo **mustContain** a uma classe (diretamente ou por meio de herança adicionando uma classe auxiliar).
-   Não é possível excluir qualquer **mustContain** da classe (diretamente ou por meio de herança).

Além disso, as seguintes restrições adicionais são impostas em objetos de esquema da categoria 1:

-   Você não pode alterar os seguintes atributos de um atributo category 1:

    -   **RangeLower** e **rangeUpper** (intervalo de valores).
    -   **attributeSecurityGuid** (determina a qual conjunto de propriedades o atributo pertence, se houver).

-   Não é possível alterar o **defaultObjectCategory** de uma classe Category 1.
-   Não é possível alterar a **objectCategory** de qualquer instância de uma classe Category 1.
-   Não é possível tornar uma classe ou atributo de categoria 1 desativado.
-   Não é possível alterar o **lDAPDisplayName** de uma classe ou atributo de categoria 1.
-   Não é possível renomear uma classe ou atributo de categoria 1.

 

 




