---
title: Implementação de arquivo de IEnumSTATPROPSTG-Compound
description: A implementação do arquivo composto da interface IEnumSTATPROPSTG é usada para enumerar Propriedades, resultando em estruturas STATPROPSTG, que contêm dados de propriedade estatística.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917578"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>Implementação de arquivo de IEnumSTATPROPSTG-Compound

A implementação do arquivo composto da interface [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) é usada para enumerar Propriedades, resultando em estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , que contêm dados de propriedade estatística. A implementação de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gerencia os dados estatísticos e é associada a um objeto de armazenamento de arquivo composto atual.

O Construtor na implementação COM de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) cria uma classe que lê todo o conjunto de propriedades e cria uma matriz estática que pode ser compartilhada quando **IEnumSTATPROPSTG:: clone** é chamado.

## <a name="when-to-use"></a>Quando usar

Chame a implementação do arquivo composto de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para enumerar as estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) que contêm dados sobre as propriedades dentro do conjunto de propriedades atual. Ao usar a implementação do arquivo composto das interfaces de armazenamento de propriedade, chame [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) para retornar um ponteiro para **IEnumSTATPROPSTG** para gerenciar o objeto de armazenamento de propriedade e os elementos dentro dele.

## <a name="remarks"></a>Comentários

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtém a próxima uma ou mais estruturas [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (o número é especificado pelo parâmetro *celt* ). Retornará S \_ OK se for bem-sucedido.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ignora o número de elementos especificados em *celt*. O próximo elemento a ser enumerado por meio de uma chamada para Next torna-se o elemento após os elementos ignorados. Retorna S \_ OK se os elementos *celt* foram ignorados; retorna s \_ false se menos de *celt* elementos foram ignorados.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Define o cursor para o início da enumeração. Se for bem-sucedido, retornará S \_ OK, caso contrário, retornará STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Usa o construtor para o [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) para criar uma cópia da matriz. Como a classe que constrói a matriz estática realmente contém o objeto, essa função é adicionada principalmente à contagem de referência.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 