---
title: Armazenamento estruturado
description: O armazenamento estruturado fornece persistência de arquivos e dados em COM manipulando um único arquivo como uma coleção estruturada de objetos conhecidos como armazenamentos e fluxos.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strctd de armazenamento estruturado STG
- Strctd de armazenamento estruturado STG, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294250"
---
# <a name="structured-storage"></a>Armazenamento estruturado

## <a name="purpose"></a>Finalidade

O armazenamento estruturado fornece persistência de arquivos e dados em COM manipulando um único arquivo como uma coleção estruturada de objetos conhecidos como armazenamentos e fluxos.

A finalidade do armazenamento estruturado é reduzir as penalidades de desempenho e a sobrecarga associada ao armazenamento de objetos separados em um único arquivo. O armazenamento estruturado fornece uma solução definindo como lidar com uma única entidade de arquivo como uma coleção estruturada de dois tipos de armazenamentos de objetos e fluxos por meio de uma implementação padrão chamada arquivos compostos. Isso permite que o usuário interaja e gerencie um arquivo composto como se fosse um único arquivo em vez de uma hierarquia aninhada de objetos separados.

## <a name="where-applicable"></a>Quando aplicável

O armazenamento estruturado pode ser usado em sistemas operacionais baseados em Microsoft COM.

## <a name="developer-audience"></a>Público de desenvolvedores

A documentação de armazenamento estruturado destina-se a programadores experientes de C e C++ e a desenvolvedores de sistemas baseados em COM.

O armazenamento estruturado dá suporte principalmente às linguagens de programação C e C++. no entanto, qualquer tecnologia baseada em COM também dará suporte a qualquer linguagem de programação que utilize ponteiros de interface.

Uma compreensão sólida das tecnologias COM é o pré-requisito para o uso de armazenamento estruturado de desenvolvimento.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Para obter mais informações sobre quais sistemas operacionais são necessários para usar um elemento de API específico, consulte a seção requisitos da documentação do elemento.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                               | Descrição                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visão geral](about-structured-storage.md)<br/>                 | Informações gerais sobre o armazenamento estruturado.<br/>                                                                                                                                                                                                                                                 |
| [Usando o armazenamento estruturado](using-structured-storage.md)<br/> | Usando informações para o armazenamento estruturado.<br/>                                                                                                                                                                                                                                                     |
| [Referência](structured-storage-reference.md)<br/>            | Documentação de interfaces, funções, estruturas e enumerações específicas de armazenamento estruturado.<br/>                                                                                                                                                                                             |
| [Amostras](samples.md)<br/>                                   | Exemplos de código escritos em C++. Para obter mais informações, consulte [nomes em IStorage](names-in-istorage.md), [cabeçalho do conjunto de propriedades](property-set-header.md), [seção](section.md), [armazenando conjuntos de propriedades](storing-property-sets.md)e usando o [armazenamento estruturado](using-structured-storage.md).<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O Component Object Model](../com/the-component-object-model.md)
</dt> </dl>

 

