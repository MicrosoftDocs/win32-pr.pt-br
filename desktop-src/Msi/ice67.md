---
description: ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922465"
---
# <a name="ice67"></a>ICE67

ICE67 verifica se o destino de um atalho não anunciado pertence ao mesmo componente que o próprio atalho ou se os atributos do componente de destino garantem que ele não altere os locais de instalação.

A falha em corrigir um aviso ou erro relatado por ICE67 pode fazer com que o atalho seja inválido se o componente de destino mudar de estado e o componente de origem não tiver. Por exemplo, quando o componente do arquivo de destino é definido para ser executado da origem, uma reinstalação que altera o componente para resultados locais no componente que contém o atalho que não está sendo reinstalado. Portanto, o atalho aponta para um local inválido.

Observe que, em alguns casos, o uso de um componente diferente para o atalho é inevitável. Por exemplo, se o atalho for criado no perfil do usuário e o arquivo for instalado em um diretório sem perfil, talvez você não consiga usar o mesmo componente para ambos os dados. (Isso resulta em falhas em cenários de vários usuários, como os descritos em [ICE57](ice57.md)). Nesse caso, você poderá usar atalhos anunciados para obter o comportamento desejado ou pode simplesmente garantir que o componente de destino não possa ser alterado de executar de origem para local.

## <a name="result"></a>Resultado

ICE67 retornará um erro ou um aviso se o destino de um atalho não anunciado não pertencer ao mesmo componente que o próprio atalho ou se os atributos do componente de destino não tiverem certeza de que os locais de instalação não serão alterados.

## <a name="example"></a>Exemplo

ICE67 relata o seguinte aviso e erros para o exemplo mostrado.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

O Shortcut1 é instalado pelo Component2, mas seu arquivo de destino, arquivo1, é instalado pelo Component1. O componente de destino é marcado como opcional (o que significa que ele pode ser local ou executado da origem). Uma possível situação que poderia causar um problema é se Component1 muda de execução de origem para local. Isso faria com que o Shortcut1 apontasse para um local inválido.

Para corrigir esse aviso, instale o atalho como parte de Component1 ou marque Component1 como LocalOnly ou SourceOnly.

[Tabela de arquivos](file-table.md) (parcial)



| Arquivo  | Componente\_ |
|-------|-------------|
| Arquivo1 | Component1  |



 

[Tabela de atalho](shortcut-table.md) (parcial)



| Atalho  | Componente\_ | Destino      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#Arquivo1\] |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



