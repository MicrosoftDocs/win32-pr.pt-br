---
description: Essa interface IXpsOMPrintTicketResource da API de Documento XPS fornece acesso a um tíquete de impressão existente e também a capacidade de criar um tíquete de impressão em um OM XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfaces de tíquete de impressão do OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f629e716db7098f8f6999df758fd3b73e3f82b83308a3dd68d5f247d6cd709a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867752"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfaces de tíquete de impressão do OM XPS

Essa interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) da API de Documento XPS fornece acesso a um tíquete de impressão existente e também a capacidade de criar um tíquete de impressão em um OM XPS.

## <a name="print-ticket-resources"></a>Imprimir recursos de tíquete

A interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) permite que um programa leia o conteúdo de um tíquete de impressão existente chamando o **método GetPrintTicketResource** de uma interface que dá suporte a um tíquete de impressão. Novos recursos de tíquete de impressão podem ser adicionados a uma parte do documento chamando **SetPrintTicketResource**.

Há três níveis de tíquete de impressão, que especificam o escopo do tíquete de impressão. Os níveis de tíquete de impressão são: o nível de trabalho (ou pacote), o nível do documento e o nível da página. A tabela a seguir mostra a relação entre o nível de tíquete de impressão, a interface OM XPS correspondente e os métodos usados para acessar o recurso de tíquete de impressão.

| Nível de tíquete de impressão | Interface                                                | Método Get                                                                      | Método Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Trabalho                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Documento           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| ?               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Conteúdo do tíquete de impressão

O conteúdo de um recurso de tíquete de impressão existente pode ser acessado lendo o fluxo associado ao recurso. O [**método GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) da interface [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) retorna o ponteiro para um fluxo somente leitura que contém o conteúdo formatado em XML do tíquete de impressão. O formato do conteúdo do tíquete de impressão é descrito na [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um novo recurso de tíquete de impressão pode ser criado criando uma nova interface [**IXpsOMPrintTicketResource.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) Um tíquete de impressão válido formatado em XML é gravado em um fluxo e um URI de parte é criado para identificar a parte do tíquete de impressão. Para obter mais informações sobre o conteúdo de um tíquete de impressão válido, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). O fluxo e o URI da parte são passados como parâmetros da chamada [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) para definir o novo recurso de tíquete de impressão e o recurso de tíquete de impressão é adicionado à parte do documento correspondente chamando o **método SetPrintTicketResource** mostrado na tabela anterior.

## <a name="print-ticket-inheritance"></a>Herança de tíquete de impressão

Os tíquetes de impressão herdam as propriedades dos tíquetes de impressão com escopo maior. Por exemplo, um tíquete de impressão no nível do documento herda as propriedades do tíquete de impressão no nível do trabalho associado à sequência de documentos do documento. Da mesma forma, um tíquete de impressão no nível da página herda as propriedades do tíquete de impressão no nível do documento associado ao documento da página. Nesse processo de herança, as propriedades especificadas no tíquete de impressão de nível inferior substituem as propriedades correspondentes que, de outra forma, seriam herdadas do tíquete de impressão de nível superior.

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

 

 



