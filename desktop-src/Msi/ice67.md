---
description: ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b25f3bba6bd6efaf20b55982524840348f39e8717dc53b7699a6f5f2886df01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787386"
---
# <a name="ice67"></a>ICE67

ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.

A falha ao corrigir um aviso ou erro relatado pelo ICE67 poderá fazer com que o atalho seja inválido se o componente de destino mudar de estado e o componente de origem não. Por exemplo, quando o componente do arquivo de destino é definido para ser executado da origem, uma reinstalação que altera o componente para local resulta no componente que contém o atalho que não está sendo reinstalado. Portanto, o atalho aponta para um local inválido.

Observe que, em alguns casos, usar um componente diferente para o atalho é inevitável. Por exemplo, se o atalho for criado no perfil do usuário e o arquivo estiver instalado em um diretório sem perfil, talvez você não consiga usar o mesmo componente para ambas as partes de dados. (Isso resulta em falhas em cenários de vários usuários, como aqueles descritos em [ICE57](ice57.md)). Nesse caso, você pode usar atalhos anunciados para obter o comportamento desejado ou simplesmente garantir que o componente de destino não possa mudar de run-from-source para local.

## <a name="result"></a>Resultado

ICE67 retornará um erro ou um aviso se o destino de um atalho não anunciado não pertencer ao mesmo componente que o próprio atalho ou se os atributos do componente de destino não garantirem que os locais de instalação não serão alterados.

## <a name="example"></a>Exemplo

O ICE67 relata os seguintes avisos e erros para o exemplo mostrado.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 é instalado pelo Component2, mas seu arquivo de destino, File1, é instalado pelo component1. O componente de destino é marcado como opcional (o que significa que ele pode ser local ou de origem de run-from). Uma situação possível que causaria um problema é se Component1 muda de run-from-source para local. Isso faria com que Shortcut1 apontasse para um local inválido.

Para corrigir esse aviso, instale o atalho como parte do Component1 ou marque Component1 como LocalOnly ou SourceOnly.

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ |
|-------|-------------|
| Arquivo1 | Component1  |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Destino      |
|-----------|-------------|-------------|
| Atalho1 | Component2  | \[\#Arquivo1\] |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



