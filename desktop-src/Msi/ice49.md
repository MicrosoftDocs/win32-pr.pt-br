---
description: ICE49 verifica as entradas de registro padrão que não são do \_ tipo reg sz.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829477"
---
# <a name="ice49"></a>ICE49

ICE49 verifica as entradas de registro padrão que não são do tipo **reg \_ sz** .

## <a name="result"></a>Resultado

ICE49 posta um aviso se houver uma entrada de registro padrão que não seja um tipo **reg \_ sz** .

## <a name="example"></a>Exemplo

ICE49 relata o seguinte aviso para o exemplo mostrado.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

O valor ' \# 123 ' é um valor de registro **DWORD** .

[Tabela do registro](registry-table.md) (parcial)



| Registro | Nome | Valor |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Para corrigir esse aviso, altere o valor para tipo **reg \_ sz**.

Os componentes com **\_ sz não reg** são válidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de instrução condicional](conditional-statement-syntax.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



