---
description: 'Há quatro camadas para a biblioteca análise de tinta: Windows Forms, WPF, COM e a camada base. Esta seção descreve quando usar cada camada.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso da API de Análise de Tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfada58868c7fe959f832e0c1243bc91a373fb0186d8deee2f9481d78a95714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032344"
---
# <a name="ink-analysis-api-usage"></a>Uso da API de Análise de Tinta

Há quatro camadas para a biblioteca análise de tinta: Windows Forms, WPF, COM e a camada base. Esta seção descreve quando usar cada camada.

## <a name="ink-analysis-api-overview"></a>Visão geral da API de Análise de Tinta

As bibliotecas de Análise de Tinta Digital são projetadas para serem usadas em uma variedade de ambientes de programação com suporte. Há quatro camadas básicas por meio das quais seu aplicativo pode usar a Análise de Tinta. Essas camadas são:

-   A camada Windows Forms
-   A camada do WPF
-   A camada COM
-   A camada base

### <a name="windows-forms-applications"></a>Aplicativos do Windows Forms

Você pode usar a API de Análise de Tinta Em seu projeto gerenciado adicionando uma referência às seguintes bibliotecas:

-   Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)
-   Biblioteca de Análise de Documentos do Ink (IACore.dll)

No Windows Forms, você provavelmente usará as bibliotecas em conjunto com os objetos de plataforma de Tablet PC padrão encontrados no assembly da API de PC do Microsoft Tablet v1.7. Certifique-se de que você também tenha uma referência a:

-   API de PC para Tablet da Microsoft v1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Aplicativos do Presentation Framework

Você pode usar a API de Análise de Tinta Em seu projeto do WPF adicionando uma referência aos membros da Análise de Tinta Que são definidos no Sistema. Windows. Namespace de tinta no IAWinFX.dll assembly. Esse assembly é instalado pelo SDK.

### <a name="com-applications"></a>Aplicativos COM

Aplicativos COM que não são de Automação devem usar a camada COM das APIs de Análise de Tinta.

Objetos [ContextNode específicos](/previous-versions/ms551996(v=vs.100)) de tipo, como [ParagraphNode,](/previous-versions/ms580136(v=vs.100)) [InkWordNode](/previous-versions/ms580133(v=vs.100))e outros, não são usados na camada COM. Em vez disso, você deve usar [**iContextNode::AddPropertyData**](icontextnode-addpropertydata.md) na interface [**IContextNode**](icontextnode.md) padrão.

Você deve \# incluir "IACom.h". Provavelmente, você usará as bibliotecas em conjunto com o objeto Ink da plataforma tablet pc, portanto, também deve incluir \# "msinkaut.h".

### <a name="rts-and-other-applications"></a>RTS e outros aplicativos

A camada base análise de tinta funciona de maneira diferente das outras, pois ela recebe dados de ponto para análise em vez de [objetos Stroke.](/previous-versions/ms552692(v=vs.100)) Exemplos de onde você trabalharia com a camada Base diretamente em vez de usar os formulários do Windows ou camadas COM incluem aplicativos que não usam objetos de Tinta [](/previous-versions/ms583670(v=vs.100)) da Plataforma de Tablet pc de primeira geração ou aplicativos que usam as APIs [**do RealTimeStylus**](realtimestylus-class.md) para gerenciar a entrada de caneta em vez de usar os objetos de Tinta da Plataforma de Tablet PC.

## <a name="32-bit-support-only"></a>Suporte somente de 32 bits

Observe que as bibliotecas de Análise de Tinta São suportadas apenas em processos de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da análise de tinta](ink-analysis-overview.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 
