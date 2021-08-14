---
description: ICE49 verifica se há entradas padrão do Registro que não são um tipo REG \_ SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa16dfb082186fd13fccc4cde95abf35b99894cdc18e322eb3e57e67d29465ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381796"
---
# <a name="ice49"></a>ICE49

ICE49 verifica se há entradas padrão do Registro que não são um **tipo REG \_ SZ.**

## <a name="result"></a>Resultado

ICE49 posta um aviso se houver uma entrada de Registro padrão que não seja um **tipo REG \_ SZ.**

## <a name="example"></a>Exemplo

ICE49 relata o seguinte aviso para o exemplo mostrado.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

O valor ' \# 123' é um valor do Registro **DWORD.**

[Tabela do Registro](registry-table.md) (parcial)



| Registro | Name | Valor |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Para corrigir esse aviso, altere o valor para o tipo **REG \_ SZ**.

Os componentes com **REG \_ SZ não são** válidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe da instrução condicional](conditional-statement-syntax.md)
</dt> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



