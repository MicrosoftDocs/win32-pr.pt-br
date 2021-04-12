---
title: Implementação de arquivo de IEnumSTATPROPSETSTG-Compound
description: A implementação do arquivo composto da interface IEnumSTATPROPSETSTG é usada para enumerar uma matriz de estruturas STATPROPSETSTG que contêm dados de propriedade estatística.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294126"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>Implementação de arquivo de IEnumSTATPROPSETSTG-Compound

A implementação do arquivo composto da interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) é usada para enumerar uma matriz de estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) que contêm dados de propriedade estatística. A implementação de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) gerencia os dados estatísticos e está associada a um objeto de armazenamento de arquivo composto atual.

## <a name="when-to-use"></a>Quando usar

Chame os métodos de [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) para enumerar estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , cada uma fornecendo dados sobre um dos conjuntos de propriedades associados ao objeto de armazenamento de arquivo composto.

## <a name="remarks"></a>Comentários

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Obtém a próxima uma ou mais estruturas [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) (o número é especificado pelo parâmetro *celt* ). Os elementos **STATPROPSETSTG** fornecidos por meio de uma chamada para a implementação do arquivo composto de [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) seguem estas regras:

-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) não puder fornecer STATPROPSETSTG. fmtid, zeros serão gravados nesse membro. Isso ocorre quando o conjunto de propriedades não tem um nome predefinido (como \\ 005SummaryInformation) e não é um valor válido.
-   O conjunto de propriedades DocumentSummaryInformation e UserDefined é especial, pois pode ter duas seções de conjunto de propriedades. Esse conjunto de propriedades é descrito na seção [DocumentSummaryInformation e conjuntos de propriedades definidas pelo UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). A segunda seção é chamada de propriedades de User-Defined. Cada seção é identificada com um FMTID (identificador de formato exclusivo). Quando [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) é usado para enumerar conjuntos de propriedades, o conjunto de propriedades User-Defined não será enumerado.

> [!Note]  
> Se você sempre criar um conjunto de propriedades usando [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), então, porque um "GUID de caractere" é criado para o nome de armazenamento, [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) retornará um FMTID válido, para o conjunto de propriedades \[ STATPROPSETSTG. FMTID \] .

 

-   O membro STATPROPSETSTG. grfFlags não reflete necessariamente se o conjunto de propriedades é ANSI ou não. Se PROPSETFLAG \_ ANSI for definido, o conjunto de propriedades será definitivamente ANSI. Se PROPSETFLAG \_ ANSI estiver claro, o conjunto de propriedades poderá ser Unicode ou não-Unicode, pois não é possível informar se ele é ANSI sem abri-lo.
-   O membro STATPROPSETSTG. grfFlags reflete se o conjunto de propriedades é simples ou não, portanto, a configuração do sinalizador de PROPSETFLAG \_ não simples é sempre válida.
-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) não puder fornecer STATPROPSETSTG. CLSID, ele será definido como todos os zeros (CLSID \_ NULL). Na implementação do arquivo composto COM, isso ocorre quando o conjunto de propriedades é simples (o \_ sinalizador não simples PROPSETFLAG não é definido) ou não é simples, mas o CLSID não foi definido explicitamente. Para conjuntos de propriedades não simples, o CLSID recebido é aquele que é mantido pelo [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)subjacente.
-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) não puder fornecer os campos de hora \[ **CTime**, **mtime**, **atime** \] , cada tempo sem suporte será definido como zeros. Na implementação do arquivo composto COM, obter esses valores depende de recuperá-los da implementação de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) subjacente.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Ignora o número de elementos especificados em *celt*. Retorna S \_ OK se o número especificado de elementos for ignorado, retornará s \_ false se menos elementos do que o solicitado forem ignorados. Em qualquer outro caso, o retorna o erro apropriado.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Define o cursor para o início da enumeração. Se for bem-sucedido, retornará S \_ OK, caso contrário, retornará STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG:: clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Copia o estado de enumeração atual deste enumerador.

</dd> </dl>

 

 