---
title: Interfaces de armazenamento estruturado
description: Os serviços de armazenamento estruturados são organizados em três categorias de interfaces.
ms.assetid: a4281f07-eae4-4bcb-8d16-b6c0bd3c5b21
keywords:
- Interfaces de armazenamento estruturado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0010a0d4dec4908111c8a5bb939f795f0a2b2eb3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105756356"
---
# <a name="structured-storage-interfaces"></a>Interfaces de armazenamento estruturado

Os serviços de armazenamento estruturados são organizados em três categorias de [interfaces](interfaces.md). Cada conjunto representa um nível sucessivo de indireção ou abstração entre um arquivo composto, os objetos que ele contém e a mídia física na qual esses componentes individuais são armazenados.

A primeira categoria de interfaces consiste em [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage). As duas primeiras interfaces definem como os objetos são armazenados em um arquivo composto. Essas interfaces fornecem métodos para abrir elementos de armazenamento, confirmar e reverter alterações, copiar e mover elementos e ler e gravar fluxos. Essas interfaces não reconhecem os formatos de dados nativos dos objetos individuais e, portanto, não têm nenhum método para salvar esses objetos no armazenamento persistente. A interface **IRootStorage** tem um único método para associar um documento composto a um nome de sistema de arquivos subjacente. Os clientes devem implementar essas interfaces para seus arquivos compostos.

A segunda categoria de interfaces consiste nas interfaces [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) , que os objetos implementam para gerenciar seus dados persistentes. Essas interfaces fornecem métodos para ler os formatos de dados de objetos individuais e, portanto, sabem como armazená-los. Os objetos são responsáveis por implementar essas interfaces porque os clientes não conhecem os formatos de dados nativos de seus objetos aninhados. No entanto, essas interfaces não têm conhecimento de mídia de armazenamento físico específica.

Uma terceira categoria consiste em uma única interface, [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), que fornece métodos para gravar arquivos em mídia física específica, como um disco rígido ou uma unidade de fita. No entanto, a maioria dos aplicativos não implementará a interface **ILockBytes** porque o com já fornece implementações para as duas situações mais comuns, que são implementação baseada em arquivo e implementação baseada em memória. O objeto de armazenamento de arquivo composto chama os métodos **ILockBytes** que você não os chama diretamente na implementação.

## <a name="compound-file-implementation-limits"></a>Limites de implementação de arquivo composto

A implementação COM da arquitetura de armazenamento estruturado é chamada de *arquivos compostos*. Os objetos de armazenamento, conforme implementados em arquivos compostos, incluem uma implementação das interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

Ponteiros para a implementação de arquivo composto dessas interfaces são adquiridos chamando a função [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) para criar um novo objeto de arquivo composto ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) para abrir um arquivo composto criado anteriormente.

Um método alternativo para adquirir um ponteiro para a implementação do arquivo composto dessas interfaces é chamar a função [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) mais antiga e limitada. Todas as quatro funções são tratadas como implementações de arquivo composto.

A implementação do arquivo composto pode ser configurada para usar os setores de 512 ou 4096 bytes, conforme definido na estrutura [**STGOPTIONS**](/windows/win32/api/coml2api/ns-coml2api-stgoptions) .

A implementação do arquivo composto de arquivos compostos está sujeita às seguintes restrições de implementação.



| Limite                                           | Arquivo composto                                                                                                                                                                      |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limites de tamanho do arquivo:                               | 512:2 gigabytes (GB) 4096: até os limites do sistema de arquivos<br/>                                                                                                                    |
| Tamanho máximo de heap necessário para elementos abertos:   | 512:4 megabytes (MB) 4096: até limites de memória virtual<br/>                                                                                                                 |
| Aberturas de raiz simultâneas (abre do mesmo arquivo): | Se STGM \_ Read e STGM \_ share \_ Deny \_ Write forem especificados, os limites serão determinados pelos limites do sistema de arquivos. Caso contrário, há um limite de 20 aberturas de raiz simultâneas do mesmo arquivo. |
| Número de elementos em um arquivo:                   | 512: ilimitado, mas o desempenho pode diminuir se o número de elementos nos milhares 4096: ilimitado<br/>                                                                         |



 

Devido ao limite de tamanho de heap de 4 MB, o número de elementos abertos no modo transacionado é normalmente limitado a vários milhares de elementos.

 

