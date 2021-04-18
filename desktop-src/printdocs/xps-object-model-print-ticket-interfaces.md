---
description: Essa interface IXpsOMPrintTicketResource da API de documento XPS fornece acesso a um tíquete de impressão existente e também à capacidade de criar um tíquete de impressão em um OM XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfaces de tíquete de impressão XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105788646"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfaces de tíquete de impressão XPS OM

Essa interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) da API de documento XPS fornece acesso a um tíquete de impressão existente e também à capacidade de criar um tíquete de impressão em um om XPS.

## <a name="print-ticket-resources"></a>Imprimir recursos de tíquete

A interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) permite que um programa Leia o conteúdo de um tíquete de impressão existente chamando o método **GetPrintTicketResource** de uma interface que dá suporte a um tíquete de impressão. Novos recursos de tíquete de impressão podem ser adicionados a uma parte de documento chamando **SetPrintTicketResource**.

Há três níveis de tíquete de impressão, que especificam o escopo do tíquete de impressão. Os níveis de tíquete de impressão são: o nível de trabalho (ou pacote), o nível do documento e o nível da página. A tabela a seguir mostra a relação entre o nível de tíquete de impressão, a interface XPS OM correspondente e os métodos usados para acessar o recurso de tíquete de impressão.

| Imprimir nível de tíquete | Interface                                                | Método Get                                                                      | Método Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Trabalho                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Documento           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| ?               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Imprimir conteúdo do tíquete

O conteúdo de um recurso de tíquete de impressão existente pode ser acessado com a leitura do fluxo associado ao recurso. O método [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) da interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) retorna o ponteiro para um fluxo somente leitura que contém o conteúdo formatado em XML do tíquete de impressão. O formato do conteúdo do tíquete de impressão é descrito na [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um novo recurso de tíquete de impressão pode ser criado com a criação de uma nova interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) . Um tíquete de impressão válido formatado em XML é gravado em um fluxo e um URI de parte é criado para identificar a parte do tíquete de impressão. Para obter mais informações sobre o conteúdo de um tíquete de impressão válido, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). O fluxo e o URI da parte são passados como parâmetros da chamada [**setContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) para definir o novo recurso de tíquete de impressão e o recurso de tíquete de impressão é adicionado à parte do documento correspondente chamando o método **SetPrintTicketResource** mostrado na tabela anterior.

## <a name="print-ticket-inheritance"></a>Herança de tíquete de impressão

Os tíquetes de impressão herdam as propriedades de tíquetes de impressão com escopo maior. Por exemplo, um tíquete de impressão em nível de documento herda as propriedades do tíquete de impressão no nível de trabalho que está associado à sequência de documentos do documento. Da mesma forma, um tíquete de impressão em nível de página herda as propriedades do tíquete de impressão em nível de documento que está associado ao documento da página. Nesse processo de herança, as propriedades especificadas no tíquete de impressão de nível inferior substituem as propriedades correspondentes que, de outra forma, seriam herdadas do tíquete de impressão de nível superior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



