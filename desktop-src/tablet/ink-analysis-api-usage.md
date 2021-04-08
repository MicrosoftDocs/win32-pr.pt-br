---
description: 'Há quatro camadas para a biblioteca de análise de tinta: Windows Forms, WPF, COM e a camada base. Esta seção descreve quando usar cada camada.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso da API de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920744"
---
# <a name="ink-analysis-api-usage"></a>Uso da API de análise de tinta

Há quatro camadas para a biblioteca de análise de tinta: Windows Forms, WPF, COM e a camada base. Esta seção descreve quando usar cada camada.

## <a name="ink-analysis-api-overview"></a>Visão geral da API de análise de tinta

As bibliotecas de análise de tinta são projetadas para serem usadas em uma variedade de ambientes de programação com suporte. Há quatro camadas básicas por meio das quais seu aplicativo pode fazer uso da análise de tinta. Essas camadas são:

-   A camada de Windows Forms
-   A camada do WPF
-   A camada COM
-   A camada base

### <a name="windows-forms-applications"></a>Aplicativos do Windows Forms

Você pode usar a API de análise de tinta em seu projeto gerenciado adicionando uma referência às seguintes bibliotecas:

-   Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)
-   Biblioteca de análise de documento de tinta (IACore.dll)

Em Windows Forms aplicativos, você provavelmente usará as bibliotecas em conjunto com os objetos de plataforma do Tablet PC padrão encontrados no assembly do Microsoft Tablet PC API v 1.7. Verifique também se você tem uma referência para:

-   Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Aplicativos do Windows Presentation Framework

Você pode usar a API de análise de tinta em seu projeto do WPF adicionando uma referência aos membros da análise de tinta que são definidos no namespace System. Windows. Ink no assembly IAWinFX.dll. Esse assembly é instalado pelo SDK.

### <a name="com-applications"></a>Aplicativos COM

Aplicativos COM não automação devem usar a camada COM das APIs de análise de tinta.

Digite objetos [ContextNode](/previous-versions/ms551996(v=vs.100)) específicos-como [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))e outros-não são usados na camada com. Em vez disso, você deve usar [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) na interface [**IContextNode**](icontextnode.md) padrão.

Você deve \# incluir "IACom. h". Você provavelmente usará as bibliotecas em conjunto com o objeto de tinta da plataforma Tablet PC; portanto, você também deve \# incluir "msinkaut. h".

### <a name="rts-and-other-applications"></a>RTS e outros aplicativos

A camada base de análise de tinta funciona de forma diferente das outras, pois ela leva dados de ponto para análise em vez de objetos [Stroke](/previous-versions/ms552692(v=vs.100)) . Exemplos de onde você trabalharia com a camada base diretamente em vez de usar as camadas Windows Forms ou COM incluem aplicativos que não usam a primeira geração de objetos de tinta da plataforma Tablet PC ou aplicativos que usam as APIs do [**RealTimeStylus**](realtimestylus-class.md) para gerenciar a entrada de caneta em vez de usar os objetos de [tinta](/previous-versions/ms583670(v=vs.100)) da plataforma Tablet PC.

## <a name="32-bit-support-only"></a>Somente suporte de 32 bits

Observe que as bibliotecas de análise de tinta só têm suporte em processos de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral da análise de tinta](ink-analysis-overview.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 
